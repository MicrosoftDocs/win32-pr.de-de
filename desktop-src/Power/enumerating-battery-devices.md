---
description: Verwenden Sie zum Auflisten der Akku Geräte auf einem lokalen Computer die setupdigetclassbinvs-Funktion.
ms.assetid: 17e3c779-91ba-4901-9435-b73dedbf0b89
title: Aufzählen von Akku Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d610feda8fd312bbefe2742da50d82a664a8ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358450"
---
# <a name="enumerating-battery-devices"></a>Aufzählen von Akku Geräten

Verwenden Sie zum Auflisten der Akku Geräte auf einem lokalen Computer die [setupdigetclassbinvs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) -Funktion. Der *ClassGuid* -Parameter ist ein Zeiger auf den **GUID- \_ DEVCLASS- \_ Akku** (in batclass. h definiert). Um alle Batterien aufzulisten, legen Sie den *enumeratorparameter* auf **null** fest, und legen Sie den *Flags* -Parameter auf " **digcf \_** " fest, der auf " \| **digcf \_ interfacedevice**" liegt. Um die Namen der Akku Geräte zu erhalten, verwenden Sie die Funktionen [setupdienumdeviceintergesichter](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces) und [setupdigetdeviceinterfacedetail](https://msdn.microsoft.com/library/ms792901.aspx) für die zurückgegebenen Daten. Um ein Datei Handle für die einzelnen Akku Geräte zu öffnen, müssen Sie die Funktion " [**foratefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " mit diesen Namen aufrufen.

Im folgenden Beispiel wird gezeigt, wie Akku Geräte auf einem lokalen Computer aufgezählt werden.


```C++
DWORD GetBatteryState()
 {
#define GBS_HASBATTERY 0x1
#define GBS_ONBATTERY  0x2
  // Returned value includes GBS_HASBATTERY if the system has a 
  // non-UPS battery, and GBS_ONBATTERY if the system is running on 
  // a battery.
  //
  // dwResult & GBS_ONBATTERY means we have not yet found AC power.
  // dwResult & GBS_HASBATTERY means we have found a non-UPS battery.

  DWORD dwResult = GBS_ONBATTERY;

  // IOCTL_BATTERY_QUERY_INFORMATION,
  // enumerate the batteries and ask each one for information.

  HDEVINFO hdev =
            SetupDiGetClassDevs(&GUID_DEVCLASS_BATTERY, 
                                0, 
                                0, 
                                DIGCF_PRESENT | DIGCF_DEVICEINTERFACE);
  if (INVALID_HANDLE_VALUE != hdev)
   {
    // Limit search to 100 batteries max
    for (int idev = 0; idev < 100; idev++)
     {
      SP_DEVICE_INTERFACE_DATA did = {0};
      did.cbSize = sizeof(did);

      if (SetupDiEnumDeviceInterfaces(hdev,
                                      0,
                                      &GUID_DEVCLASS_BATTERY,
                                      idev,
                                      &did))
       {
        DWORD cbRequired = 0;

        SetupDiGetDeviceInterfaceDetail(hdev,
                                        &did,
                                        0,
                                        0,
                                        &cbRequired,
                                        0);
        if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
         {
          PSP_DEVICE_INTERFACE_DETAIL_DATA pdidd =
            (PSP_DEVICE_INTERFACE_DETAIL_DATA)LocalAlloc(LPTR,
                                                         cbRequired);
          if (pdidd)
           {
            pdidd->cbSize = sizeof(*pdidd);
            if (SetupDiGetDeviceInterfaceDetail(hdev,
                                                &did,
                                                pdidd,
                                                cbRequired,
                                                &cbRequired,
                                                0))
             {
              // Enumerated a battery.  Ask it for information.
              HANDLE hBattery = 
                      CreateFile(pdidd->DevicePath,
                                 GENERIC_READ | GENERIC_WRITE,
                                 FILE_SHARE_READ | FILE_SHARE_WRITE,
                                 NULL,
                                 OPEN_EXISTING,
                                 FILE_ATTRIBUTE_NORMAL,
                                 NULL);
              if (INVALID_HANDLE_VALUE != hBattery)
               {
                // Ask the battery for its tag.
                BATTERY_QUERY_INFORMATION bqi = {0};

                DWORD dwWait = 0;
                DWORD dwOut;

                if (DeviceIoControl(hBattery,
                                    IOCTL_BATTERY_QUERY_TAG,
                                    &dwWait,
                                    sizeof(dwWait),
                                    &bqi.BatteryTag,
                                    sizeof(bqi.BatteryTag),
                                    &dwOut,
                                    NULL)
                    && bqi.BatteryTag)
                 {
                  // With the tag, you can query the battery info.
                  BATTERY_INFORMATION bi = {0};
                  bqi.InformationLevel = BatteryInformation;

                  if (DeviceIoControl(hBattery,
                                      IOCTL_BATTERY_QUERY_INFORMATION,
                                      &bqi,
                                      sizeof(bqi),
                                      &bi,
                                      sizeof(bi),
                                      &dwOut,
                                      NULL))
                   {
                    // Only non-UPS system batteries count
                    if (bi.Capabilities & BATTERY_SYSTEM_BATTERY)
                     {
                      if (!(bi.Capabilities & BATTERY_IS_SHORT_TERM))
                       {
                        dwResult |= GBS_HASBATTERY;
                       }

                      // Query the battery status.
                      BATTERY_WAIT_STATUS bws = {0};
                      bws.BatteryTag = bqi.BatteryTag;

                      BATTERY_STATUS bs;
                      if (DeviceIoControl(hBattery,
                                          IOCTL_BATTERY_QUERY_STATUS,
                                          &bws,
                                          sizeof(bws),
                                          &bs,
                                          sizeof(bs),
                                          &dwOut,
                                          NULL))
                       {
                        if (bs.PowerState & BATTERY_POWER_ON_LINE)
                         {
                          dwResult &= ~GBS_ONBATTERY;
                         }
                       }
                     }
                   }
                 }
                CloseHandle(hBattery);
               }
             }
            LocalFree(pdidd);
           }
         }
       }
        else  if (ERROR_NO_MORE_ITEMS == GetLastError())
         {
          break;  // Enumeration failed - perhaps we're out of items
         }
     }
    SetupDiDestroyDeviceInfoList(hdev);
   }

  //  Final cleanup:  If we didn't find a battery, then presume that we
  //  are on AC power.

  if (!(dwResult & GBS_HASBATTERY))
    dwResult &= ~GBS_ONBATTERY;

  return dwResult;
 }
```



Zum Auflisten der Akku Geräte, die mit einem Remote Computer verbunden sind, verwenden Sie die WMI-Klasse für den [**Win32- \_ Akku**](/windows/desktop/CIMWin32Prov/win32-battery) in einem Client Skript oder einer Anwendung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Setupdigetclassbinvs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[Setupdienumbinviceintergesichter](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[Setupdigetabviceinterfacedetail](https://msdn.microsoft.com/library/ms792901.aspx)
</dt> <dt>

[**IOCTL \_ Akku \_ - \_ abfragetag**](ioctl-battery-query-tag.md)
</dt> <dt>

[**IOCTL- \_ Akku \_ Abfrage \_ Informationen**](ioctl-battery-query-information.md)
</dt> <dt>

[**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md)
</dt> </dl>

 

 
