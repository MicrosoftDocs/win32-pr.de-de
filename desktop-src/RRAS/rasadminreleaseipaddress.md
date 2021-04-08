---
title: Rasadminreleaseipaddress-Rückruffunktion
description: Die rasadminreleaseipaddress-Funktion ist eine Anwendungs definierte Funktion, die von einer Drittanbieter-RAS-Server-Verwaltungs-dll exportiert wird.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- Rasadminreleaseipaddress-Rückruffunktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d58c162ebc6d340b9bd913407bc00aac87e208e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729816"
---
# <a name="rasadminreleaseipaddress-callback-function"></a><span data-ttu-id="59539-104">Rasadminreleaseipaddress-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="59539-104">RasAdminReleaseIpAddress callback function</span></span>

<span data-ttu-id="59539-105">\[Die **rasadminreleaseipaddress** -Funktion ist für die Verwendung in Windows NT 4,0 verfügbar und in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="59539-105">\[The **RasAdminReleaseIpAddress** function is available for use in Windows NT 4.0 and is unavailable in subsequent versions.</span></span> <span data-ttu-id="59539-106">Verwenden Sie stattdessen [**mpradminreleaseipaddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span><span class="sxs-lookup"><span data-stu-id="59539-106">Instead, use [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span></span>

<span data-ttu-id="59539-107">Die **rasadminreleaseipaddress** -Funktion ist eine Anwendungs definierte Funktion, die von einer Drittanbieter-RAS-Server-Verwaltungs-dll exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="59539-107">The **RasAdminReleaseIpAddress** function is an application-defined function that is exported by a third-party RAS server administration DLL.</span></span> <span data-ttu-id="59539-108">RAS ruft diese Funktion auf, um die dll zu benachrichtigen, dass der Remote Client getrennt wurde und dass die IP-Adresse freigegeben werden sollte.</span><span class="sxs-lookup"><span data-stu-id="59539-108">RAS calls this function to notify the DLL that the remote client was disconnected and that the IP address should be released.</span></span>

## <a name="syntax"></a><span data-ttu-id="59539-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="59539-109">Syntax</span></span>


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a><span data-ttu-id="59539-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="59539-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59539-111">*lpszusername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59539-111">*lpszUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59539-112">Gibt den Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge an, die den Namen eines Remote Benutzers angibt, für den zuvor mithilfe der [**rasadmingetipaddressforuser**](rasadmingetipaddressforuser.md) -Funktion eine IP-Adresse abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="59539-112">Specifies the pointer to a null-terminated Unicode string that specifies the name of a remote user for whom an IP address was previously obtained using the [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="59539-113">*lpszportname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59539-113">*lpszPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59539-114">Ein Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des Ports angibt, auf dem der von *lpszusername* angegebene Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="59539-114">Pointer to a null-terminated Unicode string that specifies the name of the port on which the user specified by *lpszUserName* is connected.</span></span>

</dd> <dt>

<span data-ttu-id="59539-115">*pipaddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59539-115">*pipAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59539-116">Zeiger auf eine **ipaddr** -Variable, die die IP-Adresse angibt, die für diesen Benutzer in einem vorherigen Aufruf von [**rasadmingetipaddressforuser**](rasadmingetipaddressforuser.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="59539-116">Pointer to an **IPADDR** variable that specifies the IP address returned for this user in a previous call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59539-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59539-117">Return value</span></span>

<span data-ttu-id="59539-118">Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="59539-118">There is no extended error information for this function; do no call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="59539-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59539-119">Remarks</span></span>

<span data-ttu-id="59539-120">Der RAS-Server ruft **die rasadminreleaseipaddress** -Funktion nur auf, wenn die Anwendung während des vorherigen Aufrufs von [**rasadmingetipaddressforuser**](rasadmingetipaddressforuser.md) für den Benutzer, der durch den *lpszusername* -Parameter angegeben wurde, **true** im *bnotifyrelease* -Parameter zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="59539-120">The RAS server calls the **RasAdminReleaseIpAddress** function only if the application returned **TRUE** in the *bNotifyRelease* parameter during the earlier call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) for the user specified by the *lpszUserName* parameter.</span></span>

<span data-ttu-id="59539-121">Das Setup Programm für eine Drittanbieter-RAS-Verwaltungs-dll muss die dll bei RAS registrieren, indem unter dem folgenden Schlüssel in der Registrierung Informationen bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="59539-121">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="59539-122">Um die dll zu registrieren, legen Sie die folgenden Werte unter diesem Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="59539-122">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="59539-123">Wertname</span><span class="sxs-lookup"><span data-stu-id="59539-123">Value name</span></span>    | <span data-ttu-id="59539-124">Wertdaten</span><span class="sxs-lookup"><span data-stu-id="59539-124">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="59539-125">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="59539-125">*DisplayName*</span></span> | <span data-ttu-id="59539-126">Eine **reg \_ SZ** -Zeichenfolge, die den benutzerfreundlichen anzeigen amen der dll enthält.</span><span class="sxs-lookup"><span data-stu-id="59539-126">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="59539-127">*Dll*</span><span class="sxs-lookup"><span data-stu-id="59539-127">*DLLPath*</span></span>     | <span data-ttu-id="59539-128">Eine **reg- \_ SZ** -Zeichenfolge, die den vollständigen Pfad der dll enthält.</span><span class="sxs-lookup"><span data-stu-id="59539-128">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="59539-129">Beispielsweise könnte der Registrierungs Eintrag für eine RAS-Verwaltungs-dll von einem fiktiven Unternehmen mit dem Namen ProElectron, Inc. wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="59539-129">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="59539-130">*Display Name*: **reg \_ SZ** : ProElectron RAS admin dll *DllPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="59539-130">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL *DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="59539-131">Das Setup Programm für eine RAS-Verwaltungs-dll sollte auch Funktionen zum Entfernen/Deinstallieren bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="59539-131">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="59539-132">Wenn ein Benutzer die dll entfernt, sollte das Setup Programm die Registrierungseinträge der dll löschen.</span><span class="sxs-lookup"><span data-stu-id="59539-132">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 