---
title: Festlegen eines Steuerungs Zugriffsrechts-ACE in der ACL eines Objekts
description: Mit ADSI legen Sie einen Steuerungs Zugriffsrechten ACE genau wie einen Eigenschafts spezifischen ACE fest, mit dem Unterschied, dass die IADsAccessControlEntry. ObjectType-Eigenschaft die rightsguid des Steuer Elements für das Zugriffsrecht ist.
ms.assetid: 454dc372-47b0-457d-8660-644fcfa59be8
ms.tgt_platform: multiple
keywords:
- Festlegen eines Steuerungs Zugriffsrechts-ACE in der ACL eines Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b870ad3ed5432060fb51fe14c29a81ce4665
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948547"
---
# <a name="setting-a-control-access-right-ace-in-an-objects-acl"></a>Festlegen eines Steuerungs Zugriffsrechts-ACE in der ACL eines Objekts

Mit ADSI legen Sie einen Steuerungs Zugriffsrechten ACE genau wie einen Eigenschafts spezifischen ACE fest, mit dem Unterschied, dass die [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft die **rightsguid** des Steuer Elements für das Zugriffsrecht ist. Beachten Sie, dass Sie auch die Win32-Sicherheits-APIs verwenden können, um ACLs für Verzeichnisobjekte festzulegen.

In der folgenden Tabelle sind die [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) -Eigenschaften für Steuerelement Zugriffsrechte aufgelistet, die verwendet werden können, um Eigenschaften für einen ACE festzulegen.



| Eigenschaft                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Für Steuerelement Zugriffsrechte, die den Zugriff auf spezielle Vorgänge durch erweiterte Rechte steuern, muss AccessMask das **AD \_ right \_ DS \_ Control \_ Access** -Flag enthalten. Für Steuerelement-Zugriffsrechte, die einen Eigenschaften Satz definieren, enthält "AccessMask" ADS right DS **\_ \_ \_ Read \_** Prop und/oder **ADS \_ right \_ DS \_ Write \_ Prop**.<br/> Für Steuerelement Zugriffsrechte, die validierte Schreibvorgänge steuern, enthält [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) Werbeeinblendungen **\_ \_ \_**.<br/> |
| [**Fahren**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)      | Dieser Wert muss das Flag für das vorhanden sein von " **ADS \_ Flag \_ Object \_ Type \_** " enthalten.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ObjektType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Dieser Wert muss das [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) -Format des **rightsguid** -Attributs des Zugriffsrechts für das Steuerelement sein. Beachten Sie, dass die GUID-Zeichenfolge in einem ACE die öffnenden und abschließenden geschweiften Klammern enthalten muss, auch wenn das **rightsguid** -Attribut des **controlAccessRight** -Objekts nicht die geschweiften Klammern enthält.                                                                                                                                     |
| [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | Entweder ist der Zugriff auf das **\_ \_ \_ \_ Objekt** für den Zugriff auf das Zugriffsrecht für den Zugriff auf das Zugriffs Steuerungs-Objekt durch den Zugriff zugelassen, um dem Vertrauens nehmer den Zugriff auf das Zugriffsrecht zu **\_ \_ \_ \_** verweigern.                                                                                                                                                                                                                                                                                                     |
| [**Stiftungs**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | Der Sicherheits Prinzipal, z. b. Benutzer, Gruppe, Computer usw., auf den der ACE angewendet wird.                                                                                                                                                                                                                                                                                                                                                                                              |



 

Weitere Informationen zum Erstellen eines ACE finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).

Weitere Informationen und ein Codebeispiel zum Festlegen eines ACE finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).

 

