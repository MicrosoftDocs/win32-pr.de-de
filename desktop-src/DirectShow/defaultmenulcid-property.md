---
description: Die dvdadm. defaultmenulcid-Eigenschaft legt die Registrierungs Einstellung für die benutzerdefinierte Standard-LCID für Menüs fest oder ruft Sie ab.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Defaultmenulcid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907fbef0d04306b5ddc4f9a59749c96573d05bb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125174"
---
# <a name="defaultmenulcid-property"></a>Defaultmenulcid (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDAdm.DefaultMenuLCID` -Eigenschaft legt die Registrierungs Einstellung für die benutzerdefinierte Standard-LCID für Menüs fest oder ruft Sie ab.

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die LCID darstellt, die in den Registrierungs Einstellungen für die DVD-Anwendung gespeichert ist. Dieser Wert ist nicht notwendigerweise identisch mit der Standardmenü Sprache, die auf der DVD erstellt wurde. Informationen zum Bereich gültiger LCIDs finden Sie in der Win32-Dokumentation im Platform SDK.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist Lese-/Schreibzugriff und hat keinen Standardwert. Wenn keine Standardmenü-LCID angegeben wird, verwendet das msdvdadm-Objekt die Sprache, die als Standardmenü Sprache auf der Festplatte gekennzeichnet ist.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Msdvdadm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



