---
description: Die DVDAdm.DefaultMenuLCID-Eigenschaft legt die Registrierungseinstellung für die benutzerdefinierte LCID für Menüs fest oder ruft sie ab.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: DefaultMenuLCID-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 939f65ad41cb184f38e2a30392030ca67066fe203f7952441cc2f77b1db95242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906890"
---
# <a name="defaultmenulcid-property"></a>DefaultMenuLCID-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDAdm.DefaultMenuLCID` -Eigenschaft legt die Registrierungseinstellung für die benutzerdefinierte STANDARD-LCID für Menüs fest oder ruft sie ab.

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a>Rückgabewert

Gibt einen Ganzzahlwert zurück, der die LCID darstellt, die in den Registrierungseinstellungen für die DVD-Anwendung gespeichert ist. Dieser Wert entspricht nicht unbedingt der Standardmenüsprache, die auf der DVD erstellt wurde. Den Bereich gültiger LCIDs finden Sie in der Win32-Dokumentation im Platform SDK.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist Lese-/Schreibzugriff ohne Standardwert. Wenn keine LCID für das Standardmenü angegeben ist, verwendet das MSDVDAdm-Objekt die Sprache, die als Standardmenüsprache auf dem Datenträger markiert ist.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MSDVDAdm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



