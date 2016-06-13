# Get_Distanse

        {
            double lat1 = 51.491594;
            double lon1 = 31.298318;

            double lat2 = 51.493935;
            double lon2 = 31.294944;

            double dist = (6371 *
                Math.Acos(Math.Cos(DegreeToRadian(lat1)) *
                Math.Cos(DegreeToRadian(lat2)) *
                Math.Cos(DegreeToRadian(lon2) - DegreeToRadian(lon1)) +
                Math.Sin(DegreeToRadian(lat1)) *
                Math.Sin(DegreeToRadian(lat2))));

            //(350m)
            Console.WriteLine("-----------dist km = " + dist);
            Console.ReadKey();
        }


        private static double DegreeToRadian(double angle)
        {
            return Math.PI * angle / 180.0;
        }
