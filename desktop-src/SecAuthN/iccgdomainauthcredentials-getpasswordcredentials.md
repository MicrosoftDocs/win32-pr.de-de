---
description: Gibt Anmeldeinformationen zurück, um einen nicht in die Domäne beigetretenen Container bei Active Directory zu authentifizieren.
title: ICcgDomainAuthCredentials::GetPasswordCredentials-Methode (ccgplugins.h)
ms.topic: reference
ms.date: 10/21/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials.GetPasswordCredentials
api_type:
- COM
api_location:
- ccgplugins.h
ms.openlocfilehash: abd70a109e491773b374ae32787760d265167baa
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387804"
---
# <a name="iccgdomainauthcredentialsgetpasswordcredentials-method"></a><span data-ttu-id="0cb94-103">ICcgDomainAuthCredentials::GetPasswordCredentials-Methode</span><span class="sxs-lookup"><span data-stu-id="0cb94-103">ICcgDomainAuthCredentials::GetPasswordCredentials method</span></span>

<span data-ttu-id="0cb94-104">Gibt Anmeldeinformationen zurück, um einen nicht in die Domäne beigetretenen Container bei Active Directory zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="0cb94-104">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb94-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cb94-105">Syntax</span></span>


```C++
HRESULT GetPasswordCredentials(
[in] LPCWSTR pluginInput, 
[out] LPWSTR* domainName, 
[out] LPWSTR* username, 
[out] LPWSTR* password);
);
```



## <a name="parameters"></a><span data-ttu-id="0cb94-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cb94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cb94-107">*pluginInput* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0cb94-107">*pluginInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb94-108">Eine von der Containerlaufzeit übergebene Eingabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0cb94-108">An input string passed in by the container runtime.</span></span> <span data-ttu-id="0cb94-109">Die Clientimplementierung verwendet die bereitgestellte Eingabezeichenfolge, um Authentifizierungsanmeldeinformationen abzurufen, die in der Regel von einem sicheren Speicheranbieter abgerufen werden, die in den Ausgabeparametern zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0cb94-109">The client implementation uses the provided input string to retrieve authentication credentials, typically from a secure storage provider, that are returned in the output parameters.</span></span> <span data-ttu-id="0cb94-110">Die Eingabezeichenfolge wird dem Host Compute Services (HCS) in einer Spezifikationsdatei für Anmeldeinformationen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0cb94-110">The input string is provided to the Host Compute Services (HCS) in a credential specification file.</span></span> <span data-ttu-id="0cb94-111">Weitere Informationen finden Sie im Abschnitt **Hinweise**.</span><span class="sxs-lookup"><span data-stu-id="0cb94-111">For more information, see the **Remarks** section.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="0cb94-112">*domainName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cb94-112">*domainName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb94-113">Der Domänenname für die Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="0cb94-113">The domain name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="0cb94-114">*Benutzername* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cb94-114">*username* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb94-115">Der Benutzername für die Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="0cb94-115">The user name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="0cb94-116">*Kennwort* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cb94-116">*password* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb94-117">Das Kennwort für die Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="0cb94-117">The password for the credentials.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cb94-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0cb94-118">Return value</span></span>

<span data-ttu-id="0cb94-119">Der Rückgabewert ist ein **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="0cb94-119">The return value is an **HRESULT**.</span></span> <span data-ttu-id="0cb94-120">Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0cb94-120">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb94-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0cb94-121">Remarks</span></span>

<span data-ttu-id="0cb94-122">Die API kann gleichzeitig aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0cb94-122">The API may be called concurrently.</span></span> <span data-ttu-id="0cb94-123">Daher muss der Entwickler sicherstellen, dass seine Implementierung threadsicher ist.</span><span class="sxs-lookup"><span data-stu-id="0cb94-123">Therefore, the developer needs to ensure that their implementation is thread safe.</span></span> <span data-ttu-id="0cb94-124">Darüber hinaus wird das COM-Objekt out-of-proc aktiviert und muss entsprechend registriert werden.</span><span class="sxs-lookup"><span data-stu-id="0cb94-124">Additionally, the COM object will be activated out-of-proc and it must be registered appropriately.</span></span> 

<span data-ttu-id="0cb94-125">Der Implementer muss einen Schlüssel unter "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses" für seine COM-CLSID hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0cb94-125">The implementer must add a key under “HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses” for their COM CLSID.</span></span> <span data-ttu-id="0cb94-126">Der Schreibzugriff auf "CCG\COMClasses" ist auf SYSTEM- und Administratorkonten beschränkt.</span><span class="sxs-lookup"><span data-stu-id="0cb94-126">Write access to “CCG\COMClasses” is restricted to SYSTEM and Administrator accounts.</span></span> 

<span data-ttu-id="0cb94-127">Im Folgenden finden Sie eine Beispieldatei für die Spezifikation von Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="0cb94-127">The following is an example credential specification file.</span></span> <span data-ttu-id="0cb94-128">Informationen zur Bereitstellung dieser Datei für Docker finden Sie unter [Ausführen eines Containers mit einem gMSA.](/virtualization/windowscontainers/manage-containers/gmsa-run-container)</span><span class="sxs-lookup"><span data-stu-id="0cb94-128">For information on supplying this file to Docker, see [Run a container with a gMSA](/virtualization/windowscontainers/manage-containers/gmsa-run-container).</span></span>

```json
{
    "CmsPlugins": [
        "ActiveDirectory"
    ],
    "DomainJoinConfig": {
        "Sid": "S-1-5-21-3700119848-2853083131-2094573802",
        "MachineAccountName": "gmsa1",
        "Guid": "630a7dd3-2d3e-4471-ae91-1d9ea2556cd5",
        "DnsTreeName": "contoso.com",
        "DnsName": "contoso.com",
        "NetBiosName": "CONTOSO"
    },
    "ActiveDirectoryConfig": {
        "GroupManagedServiceAccounts": [
            {
                "Name": "gmsa1",
                "Scope": "contoso.com"
            },
            {
                "Name": "gmsa1",
                "Scope": "CONTOSO"
            }
        ],
        "HostAccountConfig": {
            "PortableCcgVersion": "1",
            "PluginGUID": "{CFCA0441-511D-4B2A-862E-20348A78760B}",
            "PluginInput": "contoso.com:gmsaccg:<password>"
        }
    }
}

```

## <a name="examples"></a><span data-ttu-id="0cb94-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0cb94-129">Examples</span></span>

<span data-ttu-id="0cb94-130">Das folgende Beispiel zeigt eine einfache Implementierung von **ICcgDomainAuthCredentials**.</span><span class="sxs-lookup"><span data-stu-id="0cb94-130">The following example shows a simple implementation of **ICcgDomainAuthCredentials**.</span></span> <span data-ttu-id="0cb94-131">Beachten Sie, dass dieses Beispiel zur Veranschaulichung die Anmeldeinformationen durch einfache Analyse der Eingabezeichenfolge erhält.</span><span class="sxs-lookup"><span data-stu-id="0cb94-131">Note that, for illustrative purposes, this sample obtains the credentials by simply parsing the input string.</span></span> <span data-ttu-id="0cb94-132">Eine reale Implementierung würde die Anmeldeinformationen in einem sicheren Datenspeicher speichern und die Eingabezeichenfolge verwenden, um die Anmeldeinformationen zu finden.</span><span class="sxs-lookup"><span data-stu-id="0cb94-132">A real-world implementation would store the credentials in a secure data store and use the input string to locate the credential information.</span></span> <span data-ttu-id="0cb94-133">Außerdem wurden die STANDARDMÄßIGEN COM-Methodenimplementierungen in diesem Beispiel aus Kürze weggelassen.</span><span class="sxs-lookup"><span data-stu-id="0cb94-133">Also, the standard COM method implementations have been omitted from this sample for brevity.</span></span>


```C++
// UUID generated by the developer
[uuid("cfca0441-511d-4b2a-862e-20348a78760b")] 
class CCGStubPlugin : public RuntimeClass<RuntimeClassFlags<RuntimeClassType::ClassicCom>, ICcgDomainAuthCredentials >
{
   public:
    CCGStubPlugin() {}

    ~CCGStubPlugin() {}

    IFACEMETHODIMP GetPasswordCredentials(
        _In_ LPCWSTR pluginInput,
        _Outptr_ LPWSTR *domainName,
        _Outptr_ LPWSTR *username,
        _Outptr_ LPWSTR *password)
    {
        std::wstring domainParsed, userParsed, passwordParsed; 
        try
        {
            if(domainName == NULL || username == NULL || password == NULL)
            {
                return STG_E_INVALIDPARAMETER;
            }
            *domainName = NULL;
            *username = NULL;
            *password = NULL;
            wstring pluginInputString(pluginInput);
            if (count(pluginInputString.begin(), pluginInputString.end(), ':') < 2)
            {
                return CO_E_NOT_SUPPORTED;
            }
            // Extract creds of this format Domain:Username:Password
            size_t sep1 = pluginInputString.find(L":");
            size_t sep2 = pluginInputString.find(L":", sep1 + 1);
            domainParsed = pluginInputString.substr(0, sep1);
            userParsed = pluginInputString.substr(sep1 + 1, sep2 - sep1 - 1);
            passwordParsed = pluginInputString.substr(sep2 + 1);
        }
        catch (...)
        {
            return EVENT_E_INTERNALERROR;
        }

        auto userCo = wil::make_cotaskmem_string_nothrow(userParsed.c_str());
        auto passwordCo = wil::make_cotaskmem_string_nothrow(passwordParsed.c_str());
        auto domainCo = wil::make_cotaskmem_string_nothrow(domainParsed.c_str());
        if (userCo == nullptr || passwordCo == nullptr || domainCo == nullptr)
        {
            return STG_E_INSUFFICIENTMEMORY;
        }

        *domainName = domainCo.release();
        *username = userCo.release();
        *password = passwordCo.release();
        return S_OK;
    }
};
CoCreatableClass(CCGStubPlugin);

```



## <a name="requirements"></a><span data-ttu-id="0cb94-134">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0cb94-134">Requirements</span></span>




| <span data-ttu-id="0cb94-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cb94-135">Requirement</span></span> | <span data-ttu-id="0cb94-136">Wert</span><span class="sxs-lookup"><span data-stu-id="0cb94-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb94-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cb94-137">Minimum supported server</span></span> | <span data-ttu-id="0cb94-138">Windows Server, Version 2004</span><span class="sxs-lookup"><span data-stu-id="0cb94-138">Windows Server, version 2004</span></span>                                    |
| <span data-ttu-id="0cb94-139">Header</span><span class="sxs-lookup"><span data-stu-id="0cb94-139">Header</span></span>                   | <span data-ttu-id="0cb94-140">ccgplugins.h</span><span class="sxs-lookup"><span data-stu-id="0cb94-140">ccgplugins.h</span></span>   |
| <span data-ttu-id="0cb94-141">IID</span><span class="sxs-lookup"><span data-stu-id="0cb94-141">IID</span></span>                    | <span data-ttu-id="0cb94-142">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="0cb94-142">6ecda518-2010-4437-8bc3-46e752b7b172</span></span>          |



 

