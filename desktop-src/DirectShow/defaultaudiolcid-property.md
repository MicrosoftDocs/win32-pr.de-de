---
description: Die dvdadm. defaultaudiolcid-Eigenschaft legt die Registrierungs Einstellung für die benutzerdefinierte Standard-LCID für den Audiostream fest oder ruft Sie ab.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Defaultaudiolcid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe302adaa555d59b2c1dcd50d749e9afdc2de740
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346412"
---
# <a name="defaultaudiolcid-property"></a>Defaultaudiolcid (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDAdm.DefaultAudioLCID` -Eigenschaft legt die Registrierungs Einstellung für die vom Benutzer angegebene Standard-LCID für den Audiostream fest oder ruft Sie ab.

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die vom Benutzer angegebene standardaudiolcid darstellt, die in den Registrierungs Einstellungen für die DVD-Anwendung gespeichert ist. Dieser Wert ist nicht notwendigerweise identisch mit dem Standardaudiostream, wie er auf der DVD erstellt wurde.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist Lese-/Schreibzugriff und hat keinen Standardwert. Wenn keine standardaudiolcid angegeben ist, wird das msdvdadm-Objekt den Audiostream wiedergeben, der als Standarddaten Strom auf der Festplatte gekennzeichnet ist.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Msdvdadm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



