---
description: Der Übertragungsvorgang ermöglicht es einer Anwendung, eine derzeit verbundene Kommunikationssitzung an eine andere Adresse zu senden.
ms.assetid: b1027f09-74e1-4da8-b718-bb55a56dda1d
title: Übertragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724b9ade43e41ab95a5baa6dfe7d3269f4e4a174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042307"
---
# <a name="transfer"></a>Übertragen

Der Übertragungsvorgang ermöglicht es einer Anwendung, eine derzeit verbundene Kommunikationssitzung an eine andere Adresse zu senden.

TAPI bietet zwei Mechanismen zum Übertragen einer aktuellen Sitzung an eine andere Adresse. Bei *Blind Transfer* kann eine vorhandene Sitzung in einer Phase an eine angegebene Zieladresse übertragen werden. Für die *Übertragung von* Übertragungen muss zusätzlich zur aktuellen Sitzung eine Beratungssitzung vorhanden sein, die für die Übertragung eingerichtet werden soll, und anschließend wird die Übertragung abgeschlossen. Die Wahl zwischen diesen beiden Typen basiert häufig auf den Dienstanbieter Funktionen, da einige Dienstanbieter die Blind Übertragung nicht unterstützen. In einigen Fällen können Anwendungsanforderungen dazu führen, dass die beratende Übertragung die bevorzugte Methode ist, auch wenn die blinde Übertragung möglich ist.

Der Blind Übertragungsvorgang ist im Grunde mit TAPI 2 und TAPI 3 identisch, aber die beratende Übertragung folgt leicht unterschiedlichen Mustern.

**TAPI 2. x:** Die beratende Übertragung beginnt mit dem Aufrufen von [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer). Dadurch wird der vorhandene Aufruf bei der Beratung angehalten, und dieser Aufruf wird als Ziel für die nächste Anforderung zum Übertragungs Abschluss bezeichnet. Die **lineSetupTransfer** -Funktion weist auch einen-Beratungs Rückruf zu, der verwendet werden kann, um den Rückruf für die Partei einzurichten, an die der-Befehl übertragen wird. Die Anwendung kann die Erweiterung der Ziel Partei beim Beratungsgespräch (mithilfe von [**linedial**](/windows/win32/api/tapi/nf-tapi-linedial)) wählen, oder Sie kann den Rückruf abrufen und deren Belegung entfernen und stattdessen einen vorhandenen gespeicherten-Befehl aktivieren (mit [**lineunhold**](/windows/win32/api/tapi/nf-tapi-lineunhold)), wenn dies vom Switch unterstützt wird. Während der erste Aufruf bei der Beratung erfolgt und der Anruf aktiv ist, kann die Anwendung mithilfe von [**lineswaphold**](/windows/win32/api/tapi/nf-tapi-lineswaphold)zwischen diesen Aufrufen wechseln.

**TAPI 2. x:** Anwendungen vervollständigen die beratende Übertragung mithilfe von [**linecompletetransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer). Beide Aufrufe werden in den *Leerlauf* Zustand zurückversetzt.

Anwendungen können die Funktion "einmalige Übertragung" von vielen PBXs-Dateien (eine einzelne Schaltfläche zum Einrichten einer Übertragung) verwenden, indem Sie den *lpcallparameterameter* -Parameter auf den **linecallparamflags \_ onesteptransfer** -Member der [linecallparamflags- \_ Konstanten](./linecallparamflags--constants.md) festlegen, wenn Sie [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)aufrufen.

**TAPI 3. x:** Die beratende Übertragung beginnt mit der Verwendung von " [**itaddress:: anatecall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) ", um einen Beratungs Anruf an die neue Zieladresse zu erstellen. [**Itbasiccallcontrol:: Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer) wird dann für das ursprüngliche Aufruf Objekt aufgerufen, indem ein Zeiger auf das neue "Consulting callobject"-Objekt als Parameter verwendet wird. Durch den Aufruf von [**itbasiccallcontrol:: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) für das Call-Call-Objekt wird die Übertragung abgeschlossen.

Die Anwendung muss nach dem erfolgreichen Abschluss eines Übertragungs Vorgangs Sitzungs Ressourcen freigeben.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**lineblintransfer**](/windows/win32/api/tapi/nf-tapi-lineblindtransfer), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), [**linecompletetransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer).

**TAPI 3. x:** Weitere Informationen finden Sie unter [**itbasiccallcontrol:: Blind Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-blindtransfer), [**itaddress:: anatecall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall), [**itbasiccallcontrol:: Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer), [**itbasiccallcontrol:: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish).

 

 
