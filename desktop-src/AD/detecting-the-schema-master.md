---
title: Erkennen des Schema Masters
description: Active Directory Domain Services über ein Update System mit mehreren Mastern verfügen. jeder Domänen Controller enthält eine beschreibbare Kopie des Verzeichnisses.
ms.assetid: 8e096351-43f8-48ee-acb6-681d9e38e93c
ms.tgt_platform: multiple
keywords:
- Erkennen der Schema Master Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6869853cba68d7155f2091e2fe4515116944a629
ms.sourcegitcommit: f730b85cc85448913e50a7f331e10b646ea7978b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2019
ms.locfileid: "103857051"
---
# <a name="detecting-the-schema-master"></a><span data-ttu-id="6fba8-104">Erkennen des Schema Masters</span><span class="sxs-lookup"><span data-stu-id="6fba8-104">Detecting the Schema Master</span></span>

<span data-ttu-id="6fba8-105">Active Directory Domain Services über ein Update System mit mehreren Mastern verfügen. jeder Domänen Controller enthält eine beschreibbare Kopie des Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="6fba8-105">Active Directory Domain Services have a multi-master update system; every domain controller holds a writable copy of the directory.</span></span> <span data-ttu-id="6fba8-106">Schema Aktualisierungen werden an alle Domänen weitergegeben, die zur gleichen Struktur oder Gesamtstruktur gehören.</span><span class="sxs-lookup"><span data-stu-id="6fba8-106">Schema updates are propagated to all domains that belong to the same tree or forest.</span></span> <span data-ttu-id="6fba8-107">Da in Konflikt stehende Updates am Schema schwierig abgestimmt werden, können Schema Aktualisierungen nur auf einem einzelnen Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6fba8-107">Because it is difficult to reconcile conflicting updates to the schema, schema updates can only be performed at a single server.</span></span> <span data-ttu-id="6fba8-108">Der Server mit dem Recht zum Ausführen von Updates kann sich ändern, aber nur ein Server hat dieses Recht zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="6fba8-108">The server with the right to perform updates can change, but only one server will have that right at any given time.</span></span> <span data-ttu-id="6fba8-109">Dieser Server wird als Schema Master bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6fba8-109">This server is called the schema master.</span></span> <span data-ttu-id="6fba8-110">Der erste in einem Unternehmen installierte DC ist standardmäßig der Schema Master.</span><span class="sxs-lookup"><span data-stu-id="6fba8-110">The first DC installed in an enterprise is, by default, the schema master.</span></span>

<span data-ttu-id="6fba8-111">Schema Änderungen können nur auf der Ebene des Schema Masters vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="6fba8-111">Schema changes can only be made at the schema master level.</span></span> <span data-ttu-id="6fba8-112">Um zu ermitteln, welcher Domänen Controller der Schema Master ist, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="6fba8-112">To detect which DC is the schema master, perform the following steps.</span></span>

<span data-ttu-id="6fba8-113">**Erkennen des DC-Schema Masters**</span><span class="sxs-lookup"><span data-stu-id="6fba8-113">**Detecting the DC Schema Master**</span></span>

1.  <span data-ttu-id="6fba8-114">Lesen Sie das Attribut **fSMORoleOwner** des Schema Containers auf einem beliebigen Domänen Controller.</span><span class="sxs-lookup"><span data-stu-id="6fba8-114">Read the **fsmoRoleOwner** attribute of the schema container on any DC.</span></span> <span data-ttu-id="6fba8-115">Das Attribut **fSMORoleOwner** gibt den Distinguished Name (DN) des **NTDSDSA** -Objekts für den Schema Master zurück.</span><span class="sxs-lookup"><span data-stu-id="6fba8-115">The **fsmoRoleOwner** attribute returns the distinguished name (DN) of the **nTDSDSA** object for the schema master.</span></span>
2.  <span data-ttu-id="6fba8-116">Binden Sie an das **NTDSDSA** -Objekt, dessen DN Sie soeben abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="6fba8-116">Bind to the **nTDSDSA** object whose DN you just retrieved.</span></span> <span data-ttu-id="6fba8-117">Das übergeordnete Element dieses Objekts ist das Server Objekt für den Domänen Controller, der den Schema Master enthält.</span><span class="sxs-lookup"><span data-stu-id="6fba8-117">The parent of this object is the server object for the DC containing the schema master.</span></span>
3.  <span data-ttu-id="6fba8-118">Ruft den ADsPath für das übergeordnete Element des **NTDSDSA** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="6fba8-118">Get the ADsPath for the parent of the **nTDSDSA** object.</span></span> <span data-ttu-id="6fba8-119">Das übergeordnete Element ist ein Server Objekt.</span><span class="sxs-lookup"><span data-stu-id="6fba8-119">The parent is a server object.</span></span>
4.  <span data-ttu-id="6fba8-120">Binden an das Server Objekt.</span><span class="sxs-lookup"><span data-stu-id="6fba8-120">Bind to the server object.</span></span>
5.  <span data-ttu-id="6fba8-121">Holen Sie sich das **dNSHostName** -Attribut des Server Objekts.</span><span class="sxs-lookup"><span data-stu-id="6fba8-121">Get the **dNSHostName** attribute of the server object.</span></span> <span data-ttu-id="6fba8-122">Dies ist der DNS-Name des Domänen Controllers, der den Schema Master enthält.</span><span class="sxs-lookup"><span data-stu-id="6fba8-122">This is the DNS name of the DC that contains the schema master.</span></span>
6.  <span data-ttu-id="6fba8-123">Geben Sie den DNS-Namen des Schema Masters als Server und den DN als DN des Schema Containers an, der an den Schema Master gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fba8-123">Specify the DNS name of the schema master as the server and the DN as the DN of the schema container to bind to the schema master.</span></span> <span data-ttu-id="6fba8-124">Wenn der Server z. b. "DC1.fabrikam.com" und der Schema Container-DN "CN = Schema, CN = Configuration, DC = fabrikam, DC = com" war, lautet der ADsPath wie folgt.</span><span class="sxs-lookup"><span data-stu-id="6fba8-124">For example, if the server was "dc1.fabrikam.com" and the schema container DN was "cn=schema,cn=configuration,dc=fabrikam,dc=com", the ADsPath would be as follows.</span></span>
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

<span data-ttu-id="6fba8-125">Es wird empfohlen, dass Sie den Schema Master suchen und an ihn binden, um Schema Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="6fba8-125">It is recommended that you find the schema master and bind to it to make schema changes.</span></span> <span data-ttu-id="6fba8-126">Allerdings können Sie den Schema Master auf einen anderen Server verschieben.</span><span class="sxs-lookup"><span data-stu-id="6fba8-126">However, you can move the schema master to another server.</span></span>

<span data-ttu-id="6fba8-127">Um einen anderen Server zum Schema Master zu machen, kann ein entsprechend privilegierter Benutzer folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="6fba8-127">To make another server the schema master, a suitably privileged user can:</span></span>

-   <span data-ttu-id="6fba8-128">Verwenden Sie das MMC-Snap-in "Schema-Manager".</span><span class="sxs-lookup"><span data-stu-id="6fba8-128">Use the Schema Manager MMC snap-in.</span></span>
    > [!Note]
    > <span data-ttu-id="6fba8-129">Das MMC-Snap-in "Active Directory Schema" muss manuell registriert werden.</span><span class="sxs-lookup"><span data-stu-id="6fba8-129">The Active Directory Schema MMC snap-in must be registered manually.</span></span> <span data-ttu-id="6fba8-130">Um das Schema-Snap-in zu registrieren, müssen Sie den folgenden Befehl an der Eingabeaufforderung im Windows System32-Verzeichnis ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fba8-130">To register the Schema snap-in, you must run the following command from the command prompt in the Windows System32 directory.</span></span>
    >
    > <span data-ttu-id="6fba8-131">**regsvr32.exe schmmgmt.dll**</span><span class="sxs-lookup"><span data-stu-id="6fba8-131">**regsvr32.exe schmmgmt.dll**</span></span>

     

-   <span data-ttu-id="6fba8-132">Verwenden Sie das Befehlszeilenprogramm Ntdsutil.</span><span class="sxs-lookup"><span data-stu-id="6fba8-132">Use the NTDSUTIL command-line utility.</span></span>
-   <span data-ttu-id="6fba8-133">Verwenden Sie eine Drittanbieter Anwendung (eine Anwendung, die den entsprechenden LDAP-Schreibvorgang ausgibt).</span><span class="sxs-lookup"><span data-stu-id="6fba8-133">Use a third-party application (an application that issues the appropriate LDAP write).</span></span>

<span data-ttu-id="6fba8-134">Um Programm gesteuert zum Schema Master zu werden, kann eine Anwendung, die im Kontext eines entsprechend privilegierten Benutzers ausgeführt wird, einen LDAP-Schreibvorgang des operativen Attributs **becomeschemamaester** an die RootDSE auf diesem Domänen Controller ausgeben.</span><span class="sxs-lookup"><span data-stu-id="6fba8-134">To become the schema master programmatically, an application running in the context of a suitably privileged user can issue an LDAP write of the operational attribute **becomeSchemaMaster** to the rootDSE on that DC.</span></span> <span data-ttu-id="6fba8-135">Dadurch wird eine atomarische Übertragung des Schema Masters direkt vom aktuellen Inhaber zum lokalen DC initiiert.</span><span class="sxs-lookup"><span data-stu-id="6fba8-135">This initiates an atomic transfer of the schema master right from the current holder to the local DC.</span></span>

<span data-ttu-id="6fba8-136">Im folgenden Codebeispiel wird der Schema Master gefunden.</span><span class="sxs-lookup"><span data-stu-id="6fba8-136">The following code example finds the schema master.</span></span> <span data-ttu-id="6fba8-137">Die folgende Funktion bindet an den Schema Container auf dem Computer, der der Schema Master ist.</span><span class="sxs-lookup"><span data-stu-id="6fba8-137">The following function binds to the schema container on the computer that is the schema master.</span></span>


```C++
HRESULT BindToSchemaMaster(IADsContainer **ppSchemaMaster)
{
HRESULT hr = E_FAIL;
// Get rootDSE and the schema container DN.
IADs *pObject = NULL;
IADs *pTempSchema = NULL;
IADs *pNTDS = NULL;
IADs *pServer = NULL;
BSTR bstrParent;
LPOLESTR szPath = new OLECHAR[MAX_PATH];
VARIANT var, varRole,varComputer;
hr = ADsOpenObject(L"LDAP://rootDSE",
         NULL,
         NULL,
         ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
         IID_IADs,
         (void**)&pObject);
if (hr == S_OK)
{
  hr = pObject->Get(CComBSTR("schemaNamingContext"), &var);
  if (hr == S_OK)
  {
    wcscpy_s(szPath,L"LDAP://");
    wcscat_s(szPath,var.bstrVal);
    hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
             IID_IADs,
             (void**)&pTempSchema);
 
    if (hr == S_OK)
    {
      /*
      Read the fsmoRoleOwner attribute to identify which server is 
      the schema master.
      */  
      hr = pTempSchema->Get(CComBSTR("fsmoRoleOwner"), &varRole);
      if (hr == S_OK)
      {
        // The fsmoRoleOwner attribute returns the nTDSDSA object.
        // The parent is the server object.
        // Bind to NTDSDSA object and get parent.
        wcscpy_s(szPath,L"LDAP://");
        wcscat_s(szPath,varRole.bstrVal);
        hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)&pNTDS);
        if (hr == S_OK)
        {
          hr = pNTDS->get_Parent(&bstrParent);
          if (hr == S_OK)
          {
            /*
            Bind to server object and get the DNS name of 
            the server.
            */
            wcscpy_s(szPath,bstrParent);
            hr = ADsOpenObject(szPath,
               NULL,
               NULL,
               ADS_SECURE_AUTHENTICATION,
               IID_IADs,
               (void**)&pServer);
            if (hr == S_OK)
            {
              // Get the dns name of the server.
              hr = pServer->Get(CComBSTR("dNSHostName"), 
                  &varComputer);
              if (hr == S_OK)
              {
                    wcscpy_s(szPath,L"LDAP://");
                    wcscat_s(szPath,varComputer.bstrVal);
                    wcscat_s(szPath,L"/");
                    wcscat_s(szPath,var.bstrVal);
                    hr = ADsOpenObject(szPath,
                         NULL,
                         NULL,
                         ADS_SECURE_AUTHENTICATION,
                         IID_IADs,
                         (void**)ppSchemaMaster);
                    if (FAILED(hr))
                    {
                      if (*ppSchemaMaster)
                      {
                        (*ppSchemaMaster)->Release();
                        (*ppSchemaMaster) = NULL;
                      }
                    }
              }
              VariantClear(&varComputer);
            }
            if (pServer)
              pServer->Release();
          }
          SysFreeString(bstrParent);
        }
        if (pNTDS)
          pNTDS->Release();
      }
      VariantClear(&varRole);
    }
    if (pTempSchema)
      pTempSchema->Release();
  }
  VariantClear(&var);
}
if (pObject)
    pObject->Release();
 
return hr;
}
```



<span data-ttu-id="6fba8-138">Im folgenden Codebeispiel wird der DNS-Name für den Computer angezeigt, der der Schema Master ist.</span><span class="sxs-lookup"><span data-stu-id="6fba8-138">The following code example displays the DNS name for the computer that is the schema master.</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
''''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the schema
''''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the schema container
''''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the 
' schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' The fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get the parent object.
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("dNSHostName")
''''''''''''''''''''
' Display the DNS name for the computer.
''''''''''''''''''''
strText = "Schema master has the following DNS name: "& sComputer
WScript.echo strText
 
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




