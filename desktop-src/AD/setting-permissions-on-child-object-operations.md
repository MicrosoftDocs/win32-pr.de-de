---
title: Festlegen von Berechtigungen für untergeordnete Objekt Vorgänge
description: Berechtigungen, z. b. untergeordnete Elemente erstellen und untergeordnete Elemente löschen, können auch für Vorgänge für alle untergeordneten Objekte oder unter Objekte einer bestimmten Klasse erteilt oder verweigert werden.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Festlegen von Berechtigungen für untergeordnete Objekt Vorgänge
- Objekte AD, Child, Setting-Berechtigungen für untergeordnete Objekt Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d407e9b0db865c5df8d5dab53bd97f9f1afa1497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101419"
---
# <a name="setting-permissions-on-child-object-operations"></a>Festlegen von Berechtigungen für untergeordnete Objekt Vorgänge

Berechtigungen, z. b. untergeordnete Elemente erstellen und untergeordnete Elemente löschen, können auch für Vorgänge für alle untergeordneten Objekte oder unter Objekte einer bestimmten Klasse erteilt oder verweigert werden.

Das folgende Verfahren kann verwendet werden, um Berechtigungen für einen bestimmten untergeordneten Typ festzulegen.

**So legen Sie Berechtigungen für einen bestimmten untergeordneten Typ fest**

1.  Legen Sie die [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf **ADS \_ AceType \_ Access \_ Allowed \_ Object** oder **ADS \_ AceType \_ Access \_ denied \_ Object** fest.
2.  Legen Sie die [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf die GUID für die Objektklasse fest. Dies ist die **schemaIdGUID** -Eigenschaft des classSchema-Objekts, das die Objektklasse definiert. Wenn die **ObjectType** -Eigenschaft **null** ist, gilt der ACE für ein untergeordnetes Element einer beliebigen Klasse.
3.  Legen Sie die [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf den **AD-Flag- \_ \_ \_ Objekttyp \_ vorhanden** fest.

Weitere Informationen und eine Vorgehensweise zum Erstellen eines ACE finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).

Weitere Informationen und ein Codebeispiel, das verwendet werden kann, um einen ACE festzulegen, der Vorgänge für untergeordnete Objekte steuert, finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 