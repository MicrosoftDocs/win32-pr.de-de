---
description: Private Eigenschaften werden intern vom Installationsprogramm verwendet, und ihre Werte müssen vom Autor des Installationspakets in die Datenbank eingegeben oder vom Installationsprogramm während der Installation auf von der Betriebsumgebung festgelegte Werte festgelegt werden.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Private Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352427"
---
# <a name="private-properties"></a>Private Eigenschaften

Private Eigenschaften werden intern vom Installationsprogramm verwendet, und ihre Werte müssen vom Autor des Installationspakets in die Datenbank eingegeben oder vom Installationsprogramm während der Installation auf von der Betriebsumgebung festgelegte Werte festgelegt werden. Der einzige Weg, mit dem Benutzer mit privaten Eigenschaften interagieren können, ist die [Steuerung von Ereignissen](control-events.md) in der erstellten Benutzeroberfläche des Pakets. Private Eigenschaftsnamen müssen Kleinbuchstaben enthalten. Siehe [Einschränkungen für Eigenschaftsnamen](restrictions-on-property-names.md).

Private Eigenschaften beschreiben häufig die Betriebsumgebung. Wenn die Installation z. b. auf einer Windows-Plattform ausgeführt wird, legt das Installationsprogramm die [**windowsfolder**](windowsfolder.md) -Eigenschaft auf den in der Eigenschaften Tabelle angegebenen Wert fest.

Private Eigenschaftswerte können nicht in einer Befehlszeile überschrieben werden. Um eine private Eigenschaft aus einer Installation zu löschen, lassen Sie Sie aus der [Eigenschaften Tabelle](property-table.md)aus. Unter Windows XP und Windows 2000 können Sie keine private-Eigenschaft in der Benutzeroberflächen Phase der Installation festlegen und dann den Wert an die Ausführungsphase übergeben.

Eine Liste aller privaten Standardeigenschaften, die vom Installationsprogramm verwendet werden, finden Sie unter [Eigenschafts Referenz](property-reference.md). Sie können eine benutzerdefinierte private Eigenschaft definieren, indem Sie den Eigenschaftsnamen und den Anfangswert in der Eigenschaften Tabelle eingeben. Private Eigenschaftsnamen müssen immer Kleinbuchstaben enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Öffentliche Eigenschaften](public-properties.md)
</dt> </dl>

 

 



