---
title: Verwenden eines ActiveX-Datenobjekts zum Binden an ADSI-Anbieter
description: Da ADSI auch ein OLE DB-Anbieter ist, können Sie ein ActiveX Data Object (ADO) zum Herstellen einer Verbindung mit ADSI-Anbietern verwenden.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ActiveX-Datenobjekt-ADSI
- ActiveX-Datenobjekt-ADSI, verwenden von ADO zum Binden an ADSI-Anbieter
- Dienstanbieter ADSI, verwenden des ActiveX-Datenobjekts zum Binden an
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036295"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a>Verwenden eines ActiveX-Datenobjekts zum Binden an ADSI-Anbieter

Da ADSI auch ein OLE DB-Anbieter ist, können Sie ein ActiveX Data Object (ADO) zum Herstellen einer Verbindung mit ADSI-Anbietern verwenden. Wie bei anderen ADO-Anbietern müssen Sie ein neues Verbindungs Objekt erstellen und optional die Anmelde Informationen angeben, um eine Verbindung mit einem OLE DB-Anbieter herzustellen. Der Name des ADSI-OLE DB Anbieters lautet **ADSDSOObject**.

Beispiel:


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



Im vorherigen Beispiel sind Sie im Namen des aktuellen Benutzers verbunden. Um andere Anmelde Informationen anzugeben, verwenden Sie die Verbindungs Eigenschaften:


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



ADSI OLE DB definiert die folgenden Verbindungs Eigenschaften.



| Eigenschaft           | Datentyp   | Standard   |
|--------------------|-------------|-----------|
| "Benutzer-ID"          | **BSTR**    | **NULL**  |
| Password         | **BSTR**    | **NULL**  |
| "Kennwort verschlüsseln" | **Booleschen** | **FALSE** |
| "ADSI-Flag"        | **Long**    | 0         |



 

Wenn Sie OLE DB ADO verwenden, können Sie keine Bindung an ein bestimmtes Objekt durchsetzen. Sie können jedoch ein bestimmtes Objekt Abfragen und ein Resultset zurückerhalten. Nur ADSI-Anbieter, die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) unterstützen, profitieren von ADO als Programmiermodell.

Die Eigenschaft ADSI-Flag wird verwendet, um die Bindungs Authentifizierungs Option anzugeben. Bei dieser Eigenschaft kann es sich [**\_ \_ um**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) eine Kombination von Flags aus der Enumeration der ADS-Authentifizierungs Enumeration handeln.

 

 




