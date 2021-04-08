---
title: Festlegen von Berechtigungen für eine Gruppe von Eigenschaften
description: Berechtigungen können auf eine Gruppe von Eigenschaften angewendet werden.
ms.assetid: cb9f6c04-be94-45b4-ba84-2a79b7625fdd
ms.tgt_platform: multiple
keywords:
- Festlegen von Berechtigungen für eine Gruppe von Eigenschaften anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f2993a537b76b64c7e8e6323c850494b3ce306
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724409"
---
# <a name="setting-permissions-on-a-group-of-properties"></a>Festlegen von Berechtigungen für eine Gruppe von Eigenschaften

Berechtigungen können auf eine Gruppe von Eigenschaften angewendet werden. Ein Eigenschaften Satz wird durch die GUID im [**rightsguid**](/windows/desktop/ADSchema/a-rightsguid) -Attribut eines [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) -Objekts identifiziert. Diese GUID wird im [**attributeSecurityGuid**](/windows/desktop/ADSchema/a-attributesecurityguid) -Attribut des [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekts jedes Attributs in der Gruppe festgelegt.

Im folgenden Verfahren wird gezeigt, wie Sie Berechtigungen festlegen, die für eine Gruppe von Objekteigenschaften gelten.

**So legen Sie Berechtigungen fest, die für eine Gruppe von Objekteigenschaften gelten**

1.  Legen Sie die Eigenschaft [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS \_ right \_ DS \_ Read \_ Prop**, **ADS \_ right \_ DS \_ Write \_ Prop** oder beide Werte zusammen fest.
2.  Legen Sie die [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft entweder auf **ADS \_ AceType \_ Access \_ Allowed \_ Object** oder **ADS \_ AceType \_ Access \_ denied \_ Object** fest.
3.  Legen Sie die [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf die GUID des Eigenschaften Satzes fest. Dies ist die [**rightguid**](/windows/desktop/ADSchema/a-rightsguid) -Eigenschaft des [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) -Objekts, das den Eigenschaften Satz identifiziert. Diese GUID wird auch als [**attributeSecurityGuid**](/windows/desktop/ADSchema/a-attributesecurityguid) im attributeSchema-Objekt jeder Eigenschaft in der Gruppe festgelegt.
4.  Legen Sie die [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf den **AD-Flag- \_ \_ \_ Objekttyp \_ vorhanden** fest.

Beachten Sie, dass Sie nicht das Flag " **ADS \_ right \_ DS \_ Control \_ Access** " in der [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft festlegen sollten. Dieses Flag wird nur verwendet, um ein Zugriffsrecht für das Steuerelement anzugeben.

Weitere Informationen und ein Codebeispiel, das zum Festlegen von Zugriffsrechten für einen Eigenschaften Satz verwendet werden kann, finden Sie unter [Beispielcode für das Festlegen von Berechtigungen für eine Gruppe von Eigenschaften](example-code-for-setting-permissions-on-a-group-of-properties.md).

Weitere Informationen zum Erstellen eines ACE finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).

Weitere Informationen und ein Codebeispiel, das zum Festlegen eines ACE für einen Eigenschaften Satz verwendet werden kann, finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 