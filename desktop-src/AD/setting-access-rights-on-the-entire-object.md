---
title: Festlegen von Zugriffsrechten für das gesamte Objekt
description: Bestimmte Berechtigungen können nur für ein gesamtes Objekt festgelegt werden, z. b. für DELETE-und List-Inhalte. Vorgangs spezifische Berechtigungen, z. b. die Read-Berechtigung, können auch für das gesamte Objekt festgelegt werden, sodass Sie für ein gesamtes Objekt gelten.
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- Festlegen von Zugriffsrechten für das gesamte Objekt AD
- Objekte AD, Festlegen von Zugriffsrechten für
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a965b646de1ee3eba40757386fd243839cb35b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472461"
---
# <a name="setting-access-rights-on-the-entire-object"></a>Festlegen von Zugriffsrechten für das gesamte Objekt

Bestimmte Berechtigungen können nur für ein gesamtes Objekt festgelegt werden, z. b. für DELETE-und List-Inhalte. Vorgangs spezifische Berechtigungen, z. b. die Read-Berechtigung, können auch für das gesamte Objekt festgelegt werden, sodass Sie für ein gesamtes Objekt gelten.

Das folgende Verfahren kann verwendet werden, um Berechtigungen für ein gesamtes Objekt festzulegen.

**So legen Sie Berechtigungen für ein gesamtes Objekt fest**

1.  Legen Sie [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf ADS für den Zugriff auf den Zugriff auf den Zugriff auf den Zugriff auf AD- **\_ AceType \_ \_** **fest. \_ \_ \_**
2.  Legen Sie [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) und **IADsAccessControlEntry. eritedobjecttype** auf **null** fest.

Weitere Informationen zum Erstellen eines ACE finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).

Weitere Informationen und ein Codebeispiel, das zum Festlegen eines ACE verwendet werden kann, finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 