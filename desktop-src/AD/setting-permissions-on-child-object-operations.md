---
title: Festlegen von Berechtigungen für Vorgänge für untergeordnete Objekte
description: Berechtigungen, z. B. Untergeordnetes Objekt erstellen und untergeordnetes Objekt löschen, können auch für Vorgänge für alle Unterobjekte oder Unterobjekte einer bestimmten Klasse erteilt oder verweigert werden.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Festlegen von Berechtigungen für untergeordnete Objektvorgänge AD
- Objekte AD , untergeordnete Objekte, Festlegen von Berechtigungen für Untergeordnete Objektvorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f136119d5e61ea312748d5cd64cabb8c0aee0b651d8b192519dc2d74e2045cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024768"
---
# <a name="setting-permissions-on-child-object-operations"></a>Festlegen von Berechtigungen für Vorgänge für untergeordnete Objekte

Berechtigungen, z. B. Untergeordnetes Objekt erstellen und untergeordnetes Objekt löschen, können auch für Vorgänge für alle Unterobjekte oder Unterobjekte einer bestimmten Klasse erteilt oder verweigert werden.

Mit dem folgenden Verfahren können Berechtigungen für einen bestimmten Unterobjekttyp festgelegt werden.

**So legen Sie Berechtigungen für einen bestimmten Unterobjekttyp fest**

1.  Legen Sie die [**IADsAccessControlEntry.AceType-Eigenschaft**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS \_ ACETYPE \_ ACCESS ALLOWED \_ \_ OBJECT** oder **ADS \_ ACETYPE ACCESS \_ \_ DENIED OBJECT \_ fest.**
2.  Legen Sie die [**IADsAccessControlEntry.ObjectType-Eigenschaft**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf die GUID für die Objektklasse fest. Dies ist die **schemaIDGUID-Eigenschaft** des classSchema-Objekts, das die Objektklasse definiert. Wenn die **ObjectType-Eigenschaft** **NULL ist,** gilt der ACE für Unterobjekte einer beliebigen Klasse.
3.  Legen Sie die [**IADsAccessControlEntry.Flags-Eigenschaft**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS FLAG OBJECT TYPE PRESENT \_ \_ \_ \_ fest.**

Weitere Informationen und ein Verfahren zum Erstellen eines ACE finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt.](setting-access-rights-on-an-object.md)

Weitere Informationen und ein Codebeispiel, das zum Festlegen eines ACE verwendet werden kann, der Vorgänge untergeordneter Objekte steuert, finden Sie unter Beispielcode für das Festlegen eines ACE für [ein Verzeichnisobjekt.](example-code-for-setting-an-ace-on-a-directory-object.md)

 

 