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
# <a name="detecting-the-schema-master"></a>Erkennen des Schema Masters

Active Directory Domain Services über ein Update System mit mehreren Mastern verfügen. jeder Domänen Controller enthält eine beschreibbare Kopie des Verzeichnisses. Schema Aktualisierungen werden an alle Domänen weitergegeben, die zur gleichen Struktur oder Gesamtstruktur gehören. Da in Konflikt stehende Updates am Schema schwierig abgestimmt werden, können Schema Aktualisierungen nur auf einem einzelnen Server ausgeführt werden. Der Server mit dem Recht zum Ausführen von Updates kann sich ändern, aber nur ein Server hat dieses Recht zu einem bestimmten Zeitpunkt. Dieser Server wird als Schema Master bezeichnet. Der erste in einem Unternehmen installierte DC ist standardmäßig der Schema Master.

Schema Änderungen können nur auf der Ebene des Schema Masters vorgenommen werden. Um zu ermitteln, welcher Domänen Controller der Schema Master ist, führen Sie die folgenden Schritte aus.

**Erkennen des DC-Schema Masters**

1.  Lesen Sie das Attribut **fSMORoleOwner** des Schema Containers auf einem beliebigen Domänen Controller. Das Attribut **fSMORoleOwner** gibt den Distinguished Name (DN) des **NTDSDSA** -Objekts für den Schema Master zurück.
2.  Binden Sie an das **NTDSDSA** -Objekt, dessen DN Sie soeben abgerufen haben. Das übergeordnete Element dieses Objekts ist das Server Objekt für den Domänen Controller, der den Schema Master enthält.
3.  Ruft den ADsPath für das übergeordnete Element des **NTDSDSA** -Objekts ab. Das übergeordnete Element ist ein Server Objekt.
4.  Binden an das Server Objekt.
5.  Holen Sie sich das **dNSHostName** -Attribut des Server Objekts. Dies ist der DNS-Name des Domänen Controllers, der den Schema Master enthält.
6.  Geben Sie den DNS-Namen des Schema Masters als Server und den DN als DN des Schema Containers an, der an den Schema Master gebunden werden soll. Wenn der Server z. b. "DC1.fabrikam.com" und der Schema Container-DN "CN = Schema, CN = Configuration, DC = fabrikam, DC = com" war, lautet der ADsPath wie folgt.
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

Es wird empfohlen, dass Sie den Schema Master suchen und an ihn binden, um Schema Änderungen vorzunehmen. Allerdings können Sie den Schema Master auf einen anderen Server verschieben.

Um einen anderen Server zum Schema Master zu machen, kann ein entsprechend privilegierter Benutzer folgende Aktionen ausführen:

-   Verwenden Sie das MMC-Snap-in "Schema-Manager".
    > [!Note]
    > Das MMC-Snap-in "Active Directory Schema" muss manuell registriert werden. Um das Schema-Snap-in zu registrieren, müssen Sie den folgenden Befehl an der Eingabeaufforderung im Windows System32-Verzeichnis ausführen.
    >
    > **regsvr32.exe schmmgmt.dll**

     

-   Verwenden Sie das Befehlszeilenprogramm Ntdsutil.
-   Verwenden Sie eine Drittanbieter Anwendung (eine Anwendung, die den entsprechenden LDAP-Schreibvorgang ausgibt).

Um Programm gesteuert zum Schema Master zu werden, kann eine Anwendung, die im Kontext eines entsprechend privilegierten Benutzers ausgeführt wird, einen LDAP-Schreibvorgang des operativen Attributs **becomeschemamaester** an die RootDSE auf diesem Domänen Controller ausgeben. Dadurch wird eine atomarische Übertragung des Schema Masters direkt vom aktuellen Inhaber zum lokalen DC initiiert.

Im folgenden Codebeispiel wird der Schema Master gefunden. Die folgende Funktion bindet an den Schema Container auf dem Computer, der der Schema Master ist.


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



Im folgenden Codebeispiel wird der DNS-Name für den Computer angezeigt, der der Schema Master ist.


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



 

 




