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
# <a name="wzcenuminterfaces-function"></a><span data-ttu-id="3c65c-103">Wzcenumschlag Interfaces-Funktion</span><span class="sxs-lookup"><span data-stu-id="3c65c-103">WZCEnumInterfaces function</span></span>

<span data-ttu-id="3c65c-104">\[**Wzcenumschlag Interfaces** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c65c-104">\[**WZCEnumInterfaces** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="3c65c-105">Verwenden Sie stattdessen die [**wlanenuminterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="3c65c-105">Instead, use the [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) function.</span></span> <span data-ttu-id="3c65c-106">Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="3c65c-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="3c65c-107">Die **wzcenuminterfaces** -Funktion Listet alle drahtlosen LAN-Schnittstellen auf, die vom Konfigurations Dienst für drahtlose NULL-Werte verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="3c65c-107">The **WZCEnumInterfaces** function enumerates all of the wireless LAN interfaces managed by the Wireless Zero Configuration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c65c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c65c-108">Syntax</span></span>


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a><span data-ttu-id="3c65c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c65c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c65c-110">*psrvaddr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c65c-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c65c-111">Ein Zeiger auf eine Zeichenfolge, die den Namen des Computers enthält, auf dem diese Funktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c65c-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="3c65c-112">Wenn dieser Parameter **null** ist, wird der Konfigurations Dienst für drahtlose NULL-Werte auf dem lokalen Computer aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3c65c-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is enumerated on the local computer.</span></span>

<span data-ttu-id="3c65c-113">Wenn der angegebene *psrvaddr* -Parameter ein Remote Computer ist, muss der Remote Computer Remote-RPC-Aufrufe unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3c65c-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="3c65c-114">*pintfs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3c65c-114">*pIntfs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c65c-115">Ein Zeiger auf eine [**intfs- \_ Schlüssel \_ Tabellen**](intfs-key-table.md) Struktur, die eine Tabelle mit Schlüsselinformationen für alle Schnittstellen enthält.</span><span class="sxs-lookup"><span data-stu-id="3c65c-115">A pointer to a [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure that contains a table of key information for all interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c65c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c65c-116">Return value</span></span>

<span data-ttu-id="3c65c-117">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3c65c-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="3c65c-118">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Rückgabecodes sein.</span><span class="sxs-lookup"><span data-stu-id="3c65c-118">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="3c65c-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3c65c-119">Return code</span></span>                                                                                               | <span data-ttu-id="3c65c-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c65c-120">Description</span></span>                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c65c-121"><dt>**Fehler-Arena wurde durchlaufen \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3c65c-121"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="3c65c-122">Die Speicher Kontroll Blöcke wurden zerstört.</span><span class="sxs-lookup"><span data-stu-id="3c65c-122">The storage control blocks were destroyed.</span></span> <span data-ttu-id="3c65c-123">Dieser Fehler wird zurückgegeben, wenn der Konfigurations Dienst für drahtlose NULL keine internen Objekte initialisiert hat.</span><span class="sxs-lookup"><span data-stu-id="3c65c-123">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/> |
| <dl> <span data-ttu-id="3c65c-124"><dt>**RPC \_ S \_ unbekannt, \_ Wenn**</dt></span><span class="sxs-lookup"><span data-stu-id="3c65c-124"><dt>**RPC\_S\_UNKNOWN\_IF**</dt></span></span> </dl>        | <span data-ttu-id="3c65c-125">Die Schnittstelle ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="3c65c-125">The interface is unknown.</span></span><br/> <span data-ttu-id="3c65c-126">Dieser Fehler wird zurückgegeben, wenn der Konfigurations Dienst für drahtlose NULL nicht gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="3c65c-126">This error is returned if the Wireless Zero Configuration service is not started.</span></span><br/>                             |
| <dl> <span data-ttu-id="3c65c-127"><dt>**RPC \_ X \_ NULL \_ ref- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="3c65c-127"><dt>**RPC\_X\_NULL\_REF\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="3c65c-128">Ein NULL-Verweis Zeiger wurde an den Stub übermittelt.</span><span class="sxs-lookup"><span data-stu-id="3c65c-128">A null reference pointer was passed to the stub.</span></span><br/> <span data-ttu-id="3c65c-129">Dieser Fehler wird zurückgegeben, wenn der *pintfs* -Parameter **null** ist.</span><span class="sxs-lookup"><span data-stu-id="3c65c-129">This error is returned if the *pIntfs* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="3c65c-130"><dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="3c65c-130"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="3c65c-131">Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung zu verarbeiten und Arbeitsspeicher für die Abfrageergebnisse zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="3c65c-131">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="3c65c-132"><dt>**RPC- \_ Status**</dt></span><span class="sxs-lookup"><span data-stu-id="3c65c-132"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="3c65c-133">Verschiedene Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="3c65c-133">Various error codes.</span></span><br/>                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="3c65c-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c65c-134">Remarks</span></span>

<span data-ttu-id="3c65c-135">Der **dwnumintfs** -Member der [**intfs- \_ Schlüssel \_ Tabellen**](intfs-key-table.md) Struktur, auf den *pintf* zeigt, muss vor dem Aufrufen der **wzcenumschlag Interfaces** -Funktion auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3c65c-135">The **dwNumIntfs** member of the [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure pointed to by *pIntf* must be set to 0 before calling the **WZCEnumInterfaces** function.</span></span> <span data-ttu-id="3c65c-136">Außerdem muss der **pintfs** -Member auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3c65c-136">Also, the **pIntfs** member must be set to **NULL**.</span></span>

<span data-ttu-id="3c65c-137">Bei nachfolgenden Aufrufen anderer drahtlos Konfigurationsfunktionen mit drahtlos Angabe muss eine Anwendung die Schnittstelle identifizieren, auf der Sie ausgeführt wird, indem relevante Schlüsselinformationen angegeben werden, die von der **wzcenumschlag Interfaces** -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3c65c-137">For subsequent calls to other Wireless Zero Configuration functions, an application must identify the interface it is operating on by providing relevant key information returned by the **WZCEnumInterfaces** function.</span></span>

<span data-ttu-id="3c65c-138">Wenn **wzcenumschlag Interfaces** einen Fehler Erfolg zurückgibt \_ , sollte der Aufrufer [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) anrufen, um die für die zurückgegebenen Daten zugewiesenen internen Puffer freizugeben, sobald diese Informationen nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="3c65c-138">If the **WZCEnumInterfaces** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="3c65c-139">Die Header Datei " *wzcsapi. h* " und die Datei " *wzcsapi. lib* Import Library" sind im Windows SDK nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3c65c-139">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="examples"></a><span data-ttu-id="3c65c-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c65c-140">Examples</span></span>

<span data-ttu-id="3c65c-141">Im folgenden Beispiel werden die Drahtlos-LAN-Schnittstellen auf dem lokalen Computer aufgelistet, der durch den Konfigurations Dienst für drahtlose NULL verwaltet wird, und der Wert für die Schnittstellen-GUID für jede Schnittstelle ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="3c65c-141">The following example enumerates the wireless LAN interfaces on the local computer managed by the Wireless Zero Configuration service and prints out the value for interface GUID for each interface.</span></span>

> [!Note]  
> <span data-ttu-id="3c65c-142">Dieses Beispiel kann unter Windows Vista und höher nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3c65c-142">This example will fail on Windows Vista and later .</span></span>

 


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



## <a name="requirements"></a><span data-ttu-id="3c65c-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c65c-143">Requirements</span></span>



| <span data-ttu-id="3c65c-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c65c-144">Requirement</span></span> | <span data-ttu-id="3c65c-145">Wert</span><span class="sxs-lookup"><span data-stu-id="3c65c-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c65c-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c65c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3c65c-147">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c65c-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3c65c-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c65c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3c65c-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c65c-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3c65c-150">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3c65c-150">End of client support</span></span><br/>    | <span data-ttu-id="3c65c-151">Windows XP mit SP3</span><span class="sxs-lookup"><span data-stu-id="3c65c-151">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="3c65c-152">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="3c65c-152">End of server support</span></span><br/>    | <span data-ttu-id="3c65c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c65c-153">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="3c65c-154">Header</span><span class="sxs-lookup"><span data-stu-id="3c65c-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c65c-155"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c65c-155"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c65c-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3c65c-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c65c-157"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c65c-157"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c65c-158">DLL</span><span class="sxs-lookup"><span data-stu-id="3c65c-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c65c-159"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c65c-159"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c65c-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c65c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c65c-161">**intfs- \_ Schlüssel \_ Tabelle**</span><span class="sxs-lookup"><span data-stu-id="3c65c-161">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="3c65c-162">**INTF- \_ Schlüssel \_ Eintrag**</span><span class="sxs-lookup"><span data-stu-id="3c65c-162">**INTF\_KEY\_ENTRY**</span></span>](intf-key-entry.md)
</dt> <dt>

[<span data-ttu-id="3c65c-163">**Wzceapolgetinterfaceparametriams**</span><span class="sxs-lookup"><span data-stu-id="3c65c-163">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="3c65c-164">**Wzcqueryinterface**</span><span class="sxs-lookup"><span data-stu-id="3c65c-164">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="3c65c-165">**Wzkrefreshinterface**</span><span class="sxs-lookup"><span data-stu-id="3c65c-165">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
