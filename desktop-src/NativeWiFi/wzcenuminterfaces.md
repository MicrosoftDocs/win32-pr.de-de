---
description: Listet alle drahtlosen LAN-Schnittstellen auf, die vom Konfigurations Dienst für drahtlose NULL-Werte verwaltet werden.
ms.assetid: ef8a6a3e-042a-4219-baed-a82bb3e983ae
title: Wzcenumschlag Interfaces-Funktion (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEnumInterfaces
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: b2a2c886f59843dd1bf1316053c603faf4cc112a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867900"
---
# <a name="wzcenuminterfaces-function"></a>Wzcenumschlag Interfaces-Funktion

\[**Wzcenumschlag Interfaces** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt. Verwenden Sie stattdessen die [**wlanenuminterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) -Funktion. Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]

Die **wzcenuminterfaces** -Funktion Listet alle drahtlosen LAN-Schnittstellen auf, die vom Konfigurations Dienst für drahtlose NULL-Werte verwaltet werden.

## <a name="syntax"></a>Syntax


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psrvaddr* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Computers enthält, auf dem diese Funktion ausgeführt werden soll. Wenn dieser Parameter **null** ist, wird der Konfigurations Dienst für drahtlose NULL-Werte auf dem lokalen Computer aufgelistet.

Wenn der angegebene *psrvaddr* -Parameter ein Remote Computer ist, muss der Remote Computer Remote-RPC-Aufrufe unterstützen.

</dd> <dt>

*pintfs* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**intfs- \_ Schlüssel \_ Tabellen**](intfs-key-table.md) Struktur, die eine Tabelle mit Schlüsselinformationen für alle Schnittstellen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Rückgabecodes sein.



| Rückgabecode                                                                                               | Beschreibung                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Fehler-Arena wurde durchlaufen \_ \_**</dt> </dl>      | Die Speicher Kontroll Blöcke wurden zerstört. Dieser Fehler wird zurückgegeben, wenn der Konfigurations Dienst für drahtlose NULL keine internen Objekte initialisiert hat.<br/> |
| <dl> <dt>**RPC \_ S \_ unbekannt, \_ Wenn**</dt> </dl>        | Die Schnittstelle ist unbekannt.<br/> Dieser Fehler wird zurückgegeben, wenn der Konfigurations Dienst für drahtlose NULL nicht gestartet wurde.<br/>                             |
| <dl> <dt>**RPC \_ X \_ NULL \_ ref- \_ Zeiger**</dt> </dl> | Ein NULL-Verweis Zeiger wurde an den Stub übermittelt.<br/> Dieser Fehler wird zurückgegeben, wenn der *pintfs* -Parameter **null** ist.<br/>                          |
| <dl> <dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung zu verarbeiten und Arbeitsspeicher für die Abfrageergebnisse zuzuweisen.<br/>                                                  |
| <dl> <dt>**RPC- \_ Status**</dt> </dl>                | Verschiedene Fehlercodes.<br/>                                                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Der **dwnumintfs** -Member der [**intfs- \_ Schlüssel \_ Tabellen**](intfs-key-table.md) Struktur, auf den *pintf* zeigt, muss vor dem Aufrufen der **wzcenumschlag Interfaces** -Funktion auf 0 festgelegt werden. Außerdem muss der **pintfs** -Member auf **null** festgelegt werden.

Bei nachfolgenden Aufrufen anderer drahtlos Konfigurationsfunktionen mit drahtlos Angabe muss eine Anwendung die Schnittstelle identifizieren, auf der Sie ausgeführt wird, indem relevante Schlüsselinformationen angegeben werden, die von der **wzcenumschlag Interfaces** -Funktion zurückgegeben werden.

Wenn **wzcenumschlag Interfaces** einen Fehler Erfolg zurückgibt \_ , sollte der Aufrufer [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) anrufen, um die für die zurückgegebenen Daten zugewiesenen internen Puffer freizugeben, sobald diese Informationen nicht mehr benötigt werden.

> [!Note]  
> Die Header Datei " *wzcsapi. h* " und die Datei " *wzcsapi. lib* Import Library" sind im Windows SDK nicht verfügbar.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden die Drahtlos-LAN-Schnittstellen auf dem lokalen Computer aufgelistet, der durch den Konfigurations Dienst für drahtlose NULL verwaltet wird, und der Wert für die Schnittstellen-GUID für jede Schnittstelle ausgegeben.

> [!Note]  
> Dieses Beispiel kann unter Windows Vista und höher nicht ausgeführt werden.

 


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <objbase.h>
#include <wtypes.h>

#include <stdio.h>
#include <stdlib.h>

// Wzcsapi.h and Wsczapi.lib were never shipped
// So we need to LOadlibrary and call the WZCEnumInterfaces function 
// in Wzcsapi.dll in the 

typedef struct
{
    LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;

typedef struct
{
    DWORD dwNumIntfs;
    PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;

DWORD WZCEnumInterfaces(LPWSTR pSrvAddr, PINTFS_KEY_TABLE pIntfs);

//Define the function prototype
typedef DWORD (CALLBACK* WZCEnumInterfacesType)(LPWSTR, PINTFS_KEY_TABLE);

int wmain()
{
    // Declare and initialize variables.

    DWORD dwResult = 0;
//    int iRet = 0;
    
//    WCHAR GuidString[40] = {0};
     
    int i;

    /* variables used for WZCEnumInterfaces  */
    
    PINTFS_KEY_TABLE pIfList; 
    PINTF_KEY_ENTRY pIfInfo;
    
    BOOL freeResult = FALSE;
    BOOL runTimeLinkSuccess = FALSE; 
    HINSTANCE dllHandle = NULL;              
    WZCEnumInterfacesType WZCEnumInterfacesPtr = NULL;

//    wprintf(L"Sample to test WZCEnumInterface\n");
    
    //Load the dll and keep the handle to it
    dllHandle = LoadLibrary( (LPCWSTR) L"wzcsapi.dll");

    // If the handle is valid, try to get the function address. 
    if (dllHandle == NULL) {
        dwResult = GetLastError();
        wprintf(L"LoadLibrary of wzcsapi.dll failed with error: %d\n", dwResult);
        if (dwResult ==  ERROR_MOD_NOT_FOUND)
            wprintf(L"Error: The specified module could not be found\n");
        return 1;
    }
    else  
    { 
        //Get pointer to our function using GetProcAddress:
        WZCEnumInterfacesPtr = (WZCEnumInterfacesType) GetProcAddress(dllHandle,
         "WZCEnumInterfaces");

        if (WZCEnumInterfacesPtr != NULL)
            runTimeLinkSuccess = TRUE;
        else {
            dwResult = GetLastError();   
            wprintf(L"GetProcAddress of WZCEnumInterfaces failed with error: %d\n", dwResult);
            return 1;
        }    
             
        // The function address is valid, allocate some memory for pIflist
        pIfList = (PINTFS_KEY_TABLE) LocalAlloc(LMEM_ZEROINIT,4096);
        if (pIfList == NULL) {    
            wprintf(L"Unable to allocate memory to store INTFS_KEY_TABLE\n");
            freeResult = FreeLibrary(dllHandle);
            return 1;
        }    

        // If the function address is valid, call the function. 
        if (runTimeLinkSuccess)
        {
            dwResult = WZCEnumInterfacesPtr(NULL, pIfList); 
            if (dwResult != ERROR_SUCCESS)  {
                wprintf(L"WZCEnumInterfaces failed with error: %u\n", dwResult);
                // FormatMessage can be used to find out why the function failed
                  //Free the library:
                freeResult = FreeLibrary(dllHandle);
                return 1;
            }
            else {
                wprintf(L"Num Entries: %lu\n", pIfList->dwNumIntfs);

                for (i = 0; i < (int) pIfList->dwNumIntfs; i++) {
                    pIfInfo = &pIfList->pIntfs[i];
                    if (pIfInfo->wszGuid == NULL)
                        wprintf(L"  InterfaceGUID[%d]: NULL\n",i);
                    else
                        wprintf(L"  InterfaceGUID[%d]: %ws\n",i, pIfInfo->wszGuid);
                    
                }    
            }
            wprintf(L"\n");
        }
        
        freeResult = FreeLibrary(dllHandle);
    }

    if (pIfList != NULL) {
        LocalFree(pIfList);
        pIfList = NULL;
    }
    return 0;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows XP mit SP3<br/>                                                         |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Wzcsapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**intfs- \_ Schlüssel \_ Tabelle**](intfs-key-table.md)
</dt> <dt>

[**INTF- \_ Schlüssel \_ Eintrag**](intf-key-entry.md)
</dt> <dt>

[**Wzceapolgetinterfaceparametriams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**Wzcqueryinterface**](wzcqueryinterface.md)
</dt> <dt>

[**Wzkrefreshinterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
