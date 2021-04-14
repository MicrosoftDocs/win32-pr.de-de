---
description: Die dvdadm. defaultsubpicturelcid-Eigenschaft legt die Registrierungs Einstellung für die benutzerdefinierte Standard-LCID für den subbildstream fest oder ruft Sie ab.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Defaultsubpicturelcid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522784"
---
# <a name="defaultsubpicturelcid-property"></a>Defaultsubpicturelcid (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDAdm.DefaultSubpictureLCID` -Eigenschaft legt die Registrierungs Einstellung für die vom Benutzer angegebene Standard-LCID für den subbildstream fest oder ruft Sie ab.

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die vom Benutzer angegebene Standard Teilbild-LCID darstellt, wie in den Registrierungs Einstellungen für die DVD-Anwendung gespeichert. Dieser Wert ist nicht notwendigerweise identisch mit dem standardsubbildstream, wie er auf der DVD erstellt wurde. Informationen zum Bereich gültiger LCIDs finden Sie in der Win32-Dokumentation im Platform SDK.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist Lese-/Schreibzugriff und hat keinen Standardwert. Wenn keine standardmäßige unter Bild-LCID angegeben ist, wird das msdvdadm-Objekt den subbildstream wiedergeben, der als Standarddaten Strom auf der Festplatte gekennzeichnet ist.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Msdvdadm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



