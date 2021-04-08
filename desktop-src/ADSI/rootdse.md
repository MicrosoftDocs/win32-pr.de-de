---
title: RootDSE (ADSI)
description: Jeder Verzeichnisserver verfügt über einen eindeutigen Eintrag mit dem Namen RootDSE. Es werden Daten zum Server bereitstellt, z. b. die Funktionen, die unterstützte LDAP-Version und die verwendeten Namenskontexte.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f241f2b8bb08248c0579c5c23d461b8c0acf1e01
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730241"
---
# <a name="rootdse-adsi"></a>RootDSE (ADSI)

Jeder Verzeichnisserver verfügt über einen eindeutigen Eintrag mit dem Namen **rootDSE**. Es werden Daten zum Server bereitstellt, z. b. die Funktionen, die unterstützte LDAP-Version und die verwendeten Namenskontexte.

Beispielsweise zum Erstellen eines Skripts oder einer Anwendung, das in einer beliebigen Windows-Domänen Umgebung ausgeführt werden kann. Beim Herstellen einer Verbindung mit Active Directory können Sie entweder den Distinguished Name, den Servernamen oder den Domänen Namen angeben. Wenn Sie nicht über diese Informationen verfügen, können Sie das **rootDSE** -Objekt verwenden, um eine Verbindung herzustellen. Im folgenden Codebeispiel wird die Domänen Beschreibung in einer beliebigen Domäne geändert.


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



Wenn Sie das **defaultNamingContext** -Attribut von **rootDSE** erhalten, können Sie eine Bindung an die aktuelle Domäne durchführen, z. b. ist der Fabrikam **defaultNamingContext** DC = fabrikam, DC = com.

Um die Eigenschaften von **rootDSE** aufzulisten, verwenden Sie die [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) -Schnittstelle. [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) kann für diesen Task nicht verwendet werden.

Weitere Informationen finden Sie unter [Server lose Bindung und RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).

 

 