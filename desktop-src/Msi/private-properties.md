---
description: Private Eigenschaften werden intern vom Installationsprogramm verwendet, und ihre Werte müssen vom Autor des Installationspakets in die Datenbank eingegeben oder vom Installationsprogramm während der Installation auf Werte festgelegt werden, die von der Betriebsumgebung bestimmt werden.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Private Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d166f876bb953008a6920c3089fab5974ebbb05909c1b41db299212ee069dd8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558415"
---
# <a name="private-properties"></a>Private Eigenschaften

Private Eigenschaften werden intern vom Installationsprogramm verwendet, und ihre Werte müssen vom Autor des Installationspakets in die Datenbank eingegeben oder vom Installationsprogramm während der Installation auf Werte festgelegt werden, die von der Betriebsumgebung bestimmt werden. Die einzige Möglichkeit, wie ein Benutzer mit privaten Eigenschaften interagieren kann, ist das Steuern von Ereignissen [in](control-events.md) der erstellten Benutzeroberfläche des Pakets. Private Eigenschaftsnamen müssen Kleinbuchstaben enthalten. Weitere Informationen [finden Sie unter Einschränkungen für Eigenschaftsnamen.](restrictions-on-property-names.md)

Private Eigenschaften beschreiben häufig die Betriebsumgebung. Wenn die Installation beispielsweise auf einer Windows-Plattform ausgeführt wird, legt das Installationsprogramm die [**WindowsFolder-Eigenschaft**](windowsfolder.md) auf den in der Tabelle Property angegebenen Wert fest.

Private Eigenschaftswerte können nicht über eine Befehlszeile überschrieben werden. Um eine private Eigenschaft aus einer Installation zu löschen, lassen Sie sie aus der [Eigenschaftentabelle weg.](property-table.md) Unter Windows XP und Windows 2000 können Sie keine private Eigenschaft in der Benutzeroberflächenphase der Installation festlegen und den Wert dann an die Ausführungsphase übergeben.

Eine Liste aller privaten Standardeigenschaften, die vom Installationsprogramm verwendet werden, finden Sie unter [Eigenschaftenreferenz.](property-reference.md) Sie können eine benutzerdefinierte private Eigenschaft definieren, indem Sie den Namen und Anfangswert der Eigenschaft in die Tabelle Eigenschaft eingeben. Private Eigenschaftsnamen müssen immer Kleinbuchstaben enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Öffentliche Eigenschaften](public-properties.md)
</dt> </dl>

 

 



