---
title: RootDSE (ADSI)
description: Jeder Verzeichnisserver verfügt über einen eindeutigen Eintrag namens RootDSE. Es stellt Daten zum Server bereit, z. B. seine Funktionen, die von ihm unterstützten LDAP-Versionen und die von ihm verwendeten Namenskontexte.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59176315339e7458f332e2226f880b79afa10c5afc2c5089295866f6bf93939c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770630"
---
# <a name="rootdse-adsi"></a>RootDSE (ADSI)

Jeder Verzeichnisserver verfügt über einen eindeutigen Eintrag namens **RootDSE.** Es stellt Daten zum Server bereit, z. B. seine Funktionen, die von ihm unterstützten LDAP-Versionen und die von ihm verwendeten Namenskontexte.

Beispielsweise zum Erstellen eines Skripts oder einer Anwendung, das in einer beliebigen Windows ausgeführt werden kann. Sie können beim Herstellen einer Verbindung mit Active Directory entweder den Distinguished Name, den Servernamen oder den Domänennamen angeben. Wenn Sie nicht über diese Informationen verfügen, können Sie das **RootDSE-Objekt** verwenden, um eine Verbindung herzustellen. Im folgenden Codebeispiel wird die Domänenbeschreibung in einer beliebigen Domäne geändert.


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



Durch Abrufen **des defaultNamingContext-Attributs** aus **RootDSE** können Sie eine Bindung an die aktuelle Domäne erstellen, z. B. ist der Fabrikam **defaultNamingContext** DC=Fabrikam, DC=COM.

Verwenden Sie zum Auflisten der Eigenschaften von **RootDSE** die [**IADsPropertyList-Schnittstelle.**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) kann für diese Aufgabe nicht verwendet werden.

Weitere Informationen finden Sie unter [Serverlose Bindung und RootDSE.](/windows/desktop/AD/serverless-binding-and-rootdse)

 

 