---
title: Festlegen von Zugriffsrechten für das gesamte Objekt
description: Bestimmte Berechtigungen können nur für ein gesamtes Objekt festgelegt werden, z. B. Löschen und Inhalt auflisten. Vorgangsspezifische Berechtigungen, z. B. die Leseberechtigung, können auch für das gesamte Objekt festgelegt werden, sodass sie auf ein gesamtes Objekt angewendet werden.
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- Festlegen von Zugriffsrechten für das gesamte Objekt-AD
- Objekte AD , Festlegen von Zugriffsrechten für
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cde06726b7333865fe2f4b87b87bec4383a3aeb1799ad6b8772142d5b9fd6eeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024778"
---
# <a name="setting-access-rights-on-the-entire-object"></a>Festlegen von Zugriffsrechten für das gesamte Objekt

Bestimmte Berechtigungen können nur für ein gesamtes Objekt festgelegt werden, z. B. Löschen und Inhalt auflisten. Vorgangsspezifische Berechtigungen, z. B. die Leseberechtigung, können auch für das gesamte Objekt festgelegt werden, sodass sie auf ein gesamtes Objekt angewendet werden.

Das folgende Verfahren kann verwendet werden, um Berechtigungen für ein gesamtes Objekt festzulegen.

**So legen Sie Berechtigungen für ein gesamtes Objekt fest**

1.  Legen Sie [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS \_ ACETYPE \_ ACCESS \_ ALLOWED** oder **ADS \_ ACETYPE ACCESS \_ \_ DENIED fest.**
2.  Legen Sie [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) und **IADsAccessControlEntry.InheritedObjectType** auf **NULL** fest.

Weitere Informationen zum Erstellen eines ACE finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt.](setting-access-rights-on-an-object.md)

Weitere Informationen und ein Codebeispiel, das zum Festlegen eines ACE verwendet werden kann, finden Sie unter [Beispielcode zum Festlegen eines ACE für ein Verzeichnisobjekt.](example-code-for-setting-an-ace-on-a-directory-object.md)

 

 