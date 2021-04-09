---
title: Binden mit ADsOpenObject und iadsopendsobject opendsobject
description: Die ADsOpenObject-Funktion und die iadsopendsobject opendsobject-Methode werden zum Binden an Verzeichnisdienst Objekte verwendet, wenn alternative Anmelde Informationen angegeben werden müssen und die Datenverschlüsselung erforderlich ist.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Binden mit ADsOpenObject und iadsopendsobject opendsobject ADSI
- ADSI ADSI, using, Bindung mit ADsOpenObject und iadsopendsobject opendsobject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a249aa3d51520d0d345b5a098f84480e5b5016
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039600"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a><span data-ttu-id="c9e1f-105">Binden mit ADsOpenObject und iadsopendsobject:: opendsobject</span><span class="sxs-lookup"><span data-stu-id="c9e1f-105">Binding With ADsOpenObject and IADsOpenDSObject::OpenDSObject</span></span>

<span data-ttu-id="c9e1f-106">Die [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion und die [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode werden zum Binden an Verzeichnisdienst Objekte verwendet, wenn alternative Anmelde Informationen angegeben werden müssen und die Datenverschlüsselung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-106">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method are used to bind to directory service objects when alternate credentials must be specified and when data encryption is required.</span></span>

<span data-ttu-id="c9e1f-107">Wenn möglich, sollten die Anmelde Informationen des aufrufenden Threads verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-107">The credentials of the calling thread should be used when possible.</span></span> <span data-ttu-id="c9e1f-108">Wenn jedoch alternative Anmelde Informationen verwendet werden müssen, muss die [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion oder die [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-108">However, if alternate credentials must be used, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method must be used.</span></span> <span data-ttu-id="c9e1f-109">Wenn Alternative Anmelde Informationen verwendet werden, ist es wichtig, das Kennwort nicht zwischenzuspeichern.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-109">If alternate credentials are used, it is important to not cache the password.</span></span> <span data-ttu-id="c9e1f-110">Mehrere Bindungs Vorgänge können ausgeführt werden, indem Sie den Benutzernamen und das Kennwort für den ersten Bindungs Vorgang angeben und dann nur den Benutzernamen in nachfolgenden Bindungen angeben.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-110">Multiple bind operations can be performed by specifying the user name and password for the first bind operation and then specifying only the user name in subsequent binds.</span></span> <span data-ttu-id="c9e1f-111">Das System richtet eine Sitzung beim ersten Aufruf ein und verwendet dieselbe Sitzung bei nachfolgenden Bindungs aufrufen, solange die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="c9e1f-111">The system sets up a session on the first call and uses the same session on subsequent bind calls as long as the following conditions are met:</span></span>

-   <span data-ttu-id="c9e1f-112">Derselbe Benutzername in jedem Bindungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-112">The same user name in each bind operation.</span></span>
-   <span data-ttu-id="c9e1f-113">Implementieren Sie in jedem Bindungs Vorgang eine Server lose Bindung oder eine Bindung an denselben Server.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-113">Implement serverless binding or bind to the same server in each bind operation.</span></span>
-   <span data-ttu-id="c9e1f-114">Warten Sie eine offene Sitzung, indem Sie einen Objekt Verweis von einem der Bindungs Vorgänge an einem Objekt Verweis halten.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-114">Maintain an open session by holding on to an object reference from one of the bind operations.</span></span> <span data-ttu-id="c9e1f-115">Die Sitzung wird geschlossen, wenn der letzte Objekt Verweis freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-115">The session is closed when the last object reference is released.</span></span>

<span data-ttu-id="c9e1f-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) und [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) verwenden die Windows NT [Security Support Provider-Schnittstellen (SSPI)](/windows/desktop/SecAuthN/sspi) , um Flexibilität bei Authentifizierungs Optionen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) use the Windows NT [Security Support Provider Interfaces (SSPI)](/windows/desktop/SecAuthN/sspi) to allow flexibility in authentication options.</span></span> <span data-ttu-id="c9e1f-117">Der Hauptvorteil der Verwendung dieser Schnittstellen besteht darin, den Active Directory Clients verschiedene Authentifizierungs Typen bereitzustellen und die Sitzung zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-117">The major advantage of using these interfaces is to provide different types of authentication to Active Directory clients and to encrypt the session.</span></span> <span data-ttu-id="c9e1f-118">Derzeit lässt ADSI nicht zu, dass Zertifikate übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-118">Currently, ADSI does not allow certificates to be passed in.</span></span> <span data-ttu-id="c9e1f-119">Daher können Sie SSL für die Verschlüsselung und dann die Kerberos-, NTLM-oder einfache Authentifizierung verwenden. Dies hängt davon ab, wie die Flags für den *dwReserved* -Parameter festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-119">Therefore, you can use SSL for encryption and then Kerberos, NTLM, or simple authentication, depending on how the flags are set on the *dwReserved* parameter.</span></span>

<span data-ttu-id="c9e1f-120">Es ist nicht möglich, einen bestimmten SSPI-Anbieter in ADSI anzufordern, obwohl Sie immer das höchste bevorzugte Protokoll erhalten.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-120">You cannot request a specific SSPI provider in ADSI, although you always get the highest preference protocol.</span></span> <span data-ttu-id="c9e1f-121">Bei einer Windows-Client Bindung an einen Computer, auf dem Windows ausgeführt wird, ist das Protokoll Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-121">In the case of a Windows client binding to a computer running Windows, the protocol is Kerberos.</span></span> <span data-ttu-id="c9e1f-122">Das zulassen eines Zertifikats für die Authentifizierung ist im Fall einer Webseite akzeptabel, da die Authentifizierung vor dem Ausführen der Webseite erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-122">Not allowing a certificate for authentication is acceptable in the case of a webpage because authentication occurs prior to running the webpage.</span></span>

<span data-ttu-id="c9e1f-123">Obwohl Sie mit offenen Vorgängen einen Benutzer und ein Kennwort angeben können, sollten Sie dies nicht tun.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-123">Although Open operations allow you to specify a user and password, you should not do so.</span></span> <span data-ttu-id="c9e1f-124">Geben Sie stattdessen keine Anmelde Informationen an, und verwenden Sie implizit die Anmelde Informationen des Sicherheits Kontexts des Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-124">Instead, do not specify any credentials and implicitly use the credentials of the caller's security context.</span></span> <span data-ttu-id="c9e1f-125">Geben Sie für den Benutzernamen und das Kennwort **null** an, um die Bindung an ein Verzeichnis Objekt mithilfe der Anmelde Informationen des Aufrufers mit [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)herzustellen.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-125">To bind to a directory object using the caller's credentials with [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), specify **NULL** for both user name and password.</span></span>

<span data-ttu-id="c9e1f-126">Zum Binden ohne Authentifizierung verwenden Sie schließlich das Flag **ADS \_ No \_ Authentication** .</span><span class="sxs-lookup"><span data-stu-id="c9e1f-126">Finally, to bind with no authentication, use the **ADS\_NO\_AUTHENTICATION** flag.</span></span> <span data-ttu-id="c9e1f-127">Keine Authentifizierung gibt an, dass ADSI versucht, als anonymer Benutzer an das Zielobjekt zu binden, und führt keine Authentifizierung durch.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-127">No authentication indicates that ADSI attempts to bind as an anonymous user to the target object and performs no authentication.</span></span> <span data-ttu-id="c9e1f-128">Dies entspricht der Anforderung der anonymen Bindung in LDAP und gibt an, dass alle Benutzer im Sicherheitskontext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-128">This is equivalent to requesting anonymous binding in LDAP and indicates that all users are included in the security context.</span></span>

<span data-ttu-id="c9e1f-129">Wenn die Authentifizierungsflags auf NULL festgelegt sind, führt ADSI eine einfache Bindung aus, die als Klartext gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-129">If the authentication flags are set to zero, ADSI performs a simple bind, sent as plaintext.</span></span>

> [!Caution]  
> <span data-ttu-id="c9e1f-130">Wenn ein Benutzername und ein Kennwort ohne Angabe von Authentifizierungsflags angegeben werden, werden der Benutzername und das Kennwort im Klartext über das Netzwerk übertragen, was ein Sicherheitsrisiko darstellt.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-130">If a user name and password are specified without specifying authentication flags, the user name and password are transmitted over the network in plaintext, which is a security risk.</span></span> <span data-ttu-id="c9e1f-131">Geben Sie keinen Benutzernamen und kein Kennwort an, ohne Authentifizierungsflags anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-131">Do not specify a user name and password without specifying authentication flags.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c9e1f-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9e1f-132">Examples</span></span>

<span data-ttu-id="c9e1f-133">Im folgenden Visual Basic Codebeispiel wird die Verwendung der [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-133">The following Visual Basic code example shows how to use the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span>


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



<span data-ttu-id="c9e1f-134">Im folgenden C++-Codebeispiel wird die Verwendung der [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-134">The following C++ code example shows how to use the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



<span data-ttu-id="c9e1f-135">Die [**iadsopendsobject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) -Schnittstelle kann auch in C++ verwendet werden, aber die [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion wird dupliziert.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-135">The [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface can also be used in C++, but it duplicates the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>

<span data-ttu-id="c9e1f-136">Im folgenden C++-Codebeispiel wird gezeigt, wie die [**iadsopendsobject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) -Schnittstelle verwendet wird, um denselben Bindungs Vorgang wie im obigen Codebeispiel auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-136">The following C++ code example shows how to use the [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface to perform the same bind operation as in the code example above.</span></span>


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 