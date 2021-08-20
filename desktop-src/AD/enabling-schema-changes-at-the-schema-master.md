---
title: Aktivieren von Schemaänderungen auf dem Schemamaster
description: Standardmäßig ist die Schemaänderung auf allen Windows 2000-Domänencontrollern deaktiviert.
ms.assetid: 08806a9e-283c-48d9-9557-bcb9719fc13c
ms.tgt_platform: multiple
keywords:
- Aktivieren von Schemaänderungen im Schemamaster-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251716adaae4dab153b749b4db361bf7adca9b6aca2a800cec1b9d73943c595b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191386"
---
# <a name="enabling-schema-changes-at-the-schema-master"></a>Aktivieren von Schemaänderungen auf dem Schemamaster

Standardmäßig ist die Schemaänderung auf allen Windows 2000-Domänencontrollern deaktiviert. Die Möglichkeit zum Aktualisieren des Schemas wird durch den folgenden Registrierungswert auf dem Schemamasterdomänencontroller gesteuert:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            NTDS
               Parameters
                  Schema Update Allowed
```

Dieser Registrierungswert ist ein **REG \_ DWORD-Wert.** Wenn dieser Wert nicht vorhanden ist oder 0 (null) enthält, ist die Schemaänderung deaktiviert. Wenn dieser Wert vorhanden ist und einen anderen Wert als 0 (null) enthält, wird die Schemaänderung aktiviert.

Das SCHEMA-Manager-MMC-Snap-In bietet dem Benutzer die Möglichkeit, Schemaänderungen manuell zu aktivieren oder zu deaktivieren. Die Schemaänderung kann programmgesteuert aktiviert oder deaktiviert werden, indem Sie diesen Registrierungswert auf dem Schemamasterdomänencontroller ändern.

Die folgende C++-Funktion zeigt, wie Sie bestimmen, ob das Schema auf einem angegebenen Schemamaster geändert werden kann.


```C++
HRESULT IsSchemaUpdateEnabled(
    LPTSTR pszSchemaMasterComputerName, 
    BOOL *pfEnabled)
{
    *pfEnabled = FALSE;
  
    LPTSTR szPrefix = "\\\\";
    LPTSTR pszPath = new TCHAR[lstrlen(szPrefix) + 
        lstrlen(pszSchemaMasterComputerName) + 1];
    if(!pszPath)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = E_FAIL;
    LONG lReturn;
    HKEY hKeyMachine;

    tcscpy_s(pszPath, szPrefix);
    tcscat_s(pszPath, pszSchemaMasterComputerName);
    lReturn = RegConnectRegistry(
        pszPath, 
        HKEY_LOCAL_MACHINE, 
        &hKeyMachine);
    
    delete [] pszPath;

    if (ERROR_SUCCESS == lReturn)
    {
        HKEY hKeyParameters;
        LPTSTR szKeyPath = 
          TEXT("System\\CurrentControlSet\\Services\\NTDS\\Parameters");
        LPTSTR szValueName = TEXT("Schema Update Allowed");

        lReturn = RegOpenKeyEx(
            hKeyMachine, 
            szKeyPath, 
            0, 
            KEY_READ, 
            &hKeyParameters);
        if (ERROR_SUCCESS == lReturn)
        {
            DWORD dwType;
            DWORD dwValue;
            DWORD dwSize;

            dwSize = sizeof(dwValue);
            lReturn = RegQueryValueEx(
                hKeyParameters, 
                szValueName, 
                0, 
                &dwType, 
                (LPBYTE)&dwValue, 
                &dwSize);
            if (ERROR_SUCCESS == lReturn)
            {
                *pfEnabled = (0 != dwValue);
                
                hr = S_OK;
            }
            
            RegCloseKey(hKeyParameters);
        }
    
        RegCloseKey(hKeyMachine);
    }
  
    return hr;
}
```



Die folgende C++-Funktion zeigt, wie Schemaänderungen für einen angegebenen Schemamaster aktiviert oder deaktiviert werden.


```C++
HRESULT EnableSchemaUpdate(
    LPTSTR pszSchemaMasterComputerName, 
    BOOL fEnabled)
{
    
    LPTSTR szPrefix = "\\\\";
    LPTSTR pszPath = new TCHAR[lstrlen(szPrefix) + 
        lstrlen(pszSchemaMasterComputerName) + 1];
    if(!pszPath)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = E_FAIL;
    LONG lReturn;
    HKEY hKeyMachine;

    strcpy_s(pszPath, szPrefix);
    strcat_s(pszPath, pszSchemaMasterComputerName);
    lReturn = RegConnectRegistry(
        pszPath, 
        HKEY_LOCAL_MACHINE, 
        &hKeyMachine);
    
    delete [] pszPath;

    if (ERROR_SUCCESS == lReturn)
    {
        HKEY hKeyParameters;
        LPTSTR szRelKeyPath = 
          TEXT("System\\CurrentControlSet\\Services\\NTDS\\Parameters");
        LPTSTR szValueName = TEXT("Schema Update Allowed");

        lReturn = RegOpenKeyEx(
            hKeyMachine, 
            szRelKeyPath, 
            0, 
            KEY_SET_VALUE, 
            &hKeyParameters);
        if (ERROR_SUCCESS == lReturn)
        {
            DWORD dwValue;
            DWORD dwSize;

            if(fEnabled)
            {
                dwValue = 1;
            }
            else
            {
                dwValue = 0;
            }
            
            dwSize = sizeof(dwValue);
            lReturn = RegSetValueEx(
                hKeyParameters, 
                szValueName, 
                0L, 
                REG_DWORD, 
                (LPBYTE)&dwValue, 
                dwSize);
            if (ERROR_SUCCESS == lReturn)
            {
                hr = S_OK;
            }
            
            RegCloseKey(hKeyParameters);
        }
    
        RegCloseKey(hKeyMachine);
    }
    
    return hr;
}
```



 

 




