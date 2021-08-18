---
description: Die DVDAdm.DefaultSubpictureLCID-Eigenschaft legt die Registrierungseinstellung für die benutzerdefinierte LCID für den Unterbilddatenstrom fest oder ruft sie ab.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: DefaultSubpictureLCID-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc67be112349a050df45f625fda6488c91b22dee357c820724de5842c156894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952989"
---
# <a name="defaultsubpicturelcid-property"></a>DefaultSubpictureLCID-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDAdm.DefaultSubpictureLCID` -Eigenschaft legt die Registrierungseinstellung für die benutzerdefinierte STANDARD-LCID für den Unterbilddatenstrom fest oder ruft sie ab.

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die benutzerdefinierte LCID der Standardunterbilddatei darstellt, die in den Registrierungseinstellungen für die DVD-Anwendung gespeichert ist. Dieser Wert ist nicht unbedingt identisch mit dem standardmäßigen Unterbilddatenstrom, der auf der DVD erstellt wurde. Den Bereich gültiger LCIDs finden Sie in der Win32-Dokumentation im Platform SDK.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist Lese-/Schreibzugriff ohne Standardwert. Wenn keine LCID für die Standardunterdropatur angegeben ist, gibt das MSDVDAdm-Objekt den Unterbilddatenstrom wieder, der als Standardstream auf dem Datenträger markiert ist.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MSDVDAdm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



