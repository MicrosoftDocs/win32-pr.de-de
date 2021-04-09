---
title: Festlegen von Rechten für bestimmte Objekttypen
description: Im folgenden Verfahren wird gezeigt, wie ein ACE festgelegt wird, der nur von einer bestimmten Objektklasse geerbt werden kann.
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- Festlegen von Rechten auf Objekttypen
- Objekte AD, Festlegen von Rechten auf
- Active Directory, Verwendung von, Sicherheit, Festlegen von Rechten auf Objekttypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f44cfbe753e6f92787f8269eab1f4eab4c2e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948544"
---
# <a name="setting-rights-to-specific-types-of-objects"></a>Festlegen von Rechten für bestimmte Objekttypen

Im folgenden Verfahren wird gezeigt, wie ein ACE festgelegt wird, der nur von einer bestimmten Objektklasse geerbt werden kann.

 **So legen Sie einen ACE fest, der nur von einer bestimmten Objektklasse geerbt werden kann**

1.  Legen Sie die [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf **ADS \_ AceType \_ Access \_ Allowed \_ Object** oder **ADS \_ AceType \_ Access \_ denied \_ Object** fest.
2.  Legen Sie die [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft so fest, dass Sie das \_ Flag ADS aceflag \_ erben-ACE einschließt \_ .
3.  Legen Sie die [**IADsAccessControlEntry. eritedobjecttype**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf die **schemaIdGUID** der Objektklasse fest, die den ACE erben kann.
4.  Legen Sie die [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf den angezeigten **\_ \_ \_ Objekttyp \_ ADS-Flag** fest.

> [!IMPORTANT]
> Legen Sie fest, dass die ACE-Zugriffs Steuerungs Liste den ACE **\_ \_ erben \_** soll. Außerdem müssen Sie **ADS \_ aceflag \_ \_ nur auf \_ ACE erben** , wenn der Objekttyp, für den dieser ACE gilt, nicht dem Objekttyp des Containers entspricht, in dem der ACE angegeben ist. Wenn dies nicht der Fall ist, wird der ACE auch für den Container wirksam und kann unbeabsichtigte Rechte gewähren.

 

Weitere Informationen und Codebeispiele, die verwendet werden können, um diese Art von ACE festzulegen, finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 