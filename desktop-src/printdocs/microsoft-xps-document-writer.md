---
description: Der Microsoft XPS Document Writer (MXDW) ist ein Drucker-zu-Datei-Treiber, mit dem eine Windows-Anwendung XPS-Dokument Dateien (XML Paper Specification) in Windows-Versionen ab Windows XP mit Service Pack 2 (SP2) erstellen kann.
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Microsoft XPS Document Writer (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353963"
---
# <a name="microsoft-xps-document-writer-mxdw"></a>Microsoft XPS Document Writer (MXDW)

Der Microsoft XPS Document Writer (MXDW) ist ein Drucker-zu-Datei-Treiber, mit dem eine Windows-Anwendung XPS-Dokument Dateien (XML Paper Specification) in Windows-Versionen ab Windows XP mit Service Pack 2 (SP2) erstellen kann. Die Verwendung von MXDW ermöglicht es einer Windows-Anwendung, den Inhalt als XPS-Dokument zu speichern, ohne den Programmcode der Anwendung zu ändern.

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Als Benutzer wählen Sie das MXDW aus, wenn Sie ein XPS-Dokument aus einer Windows-Anwendung erstellen möchten, die nicht über die Option zum Speichern des Inhalts als XPS-Dokument verfügt.

Als Anwendungsentwickler empfiehlt es sich, MXDW für Benutzer zu empfehlen, die XPS-Dokumente erstellen möchten, wenn Ihre Anwendung nicht die Option zum Speichern als XPS-Dokument bietet. Weitere Informationen zu XML Paper Specification und XPS-Dokumenten finden Sie unter [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) und [XPS Specification und Lizenz Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).

MXDW wird automatisch unter Windows Vista und höheren Versionen von Windows installiert und kann unter Windows XP mit SP2 und Windows Server 2003 heruntergeladen und installiert werden.

## <a name="installation"></a>Installation

Unter Windows Vista und höheren Versionen von Windows wird MXDW bei der Installation des Betriebssystems automatisch installiert.

**Windows XP mit SP2 und Windows Server 2003**: Laden Sie entweder .NET Framework 3,0 oder das XPS Essentials Pack aus dem [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx)herunter, und installieren Sie es.

## <a name="how-to-use"></a>Verwendung

Bei der Installation wird MXDW als verfügbare Druck Warteschlange im Dialogfeld Drucken angezeigt, das von einer Anwendung angezeigt wird. Wenn MXDW als Drucker ausgewählt ist, wird der Benutzer aufgefordert, den Dateinamen zu erstellen, der als XPS-Dokument erstellt wird, das die Ausgabe der Anwendung erfasst.

Die folgende Abbildung zeigt, wie MXDW im Dialogfeld allgemeiner Druck von Windows Vista als Drucker ausgewählt wird.

![ein Bild des Dialog Felds drucken, das die Auswahl von Microsoft XPS Document Writer (MXDW) anzeigt.](images/choosingmxdwinvista.gif)

Anwendungsentwickler können die Ausgabe von MXDW mithilfe der [MXDW-Konfigurationseinstellungen](mxdw-configuration-settings.md)anpassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[XPS-Spezifikation und Lizenz Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[isXPS-Konformitäts Tool](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))
</dt> <dt>

[MXDW-Konfigurationseinstellungen](mxdw-configuration-settings.md)
</dt> </dl>

 

 
