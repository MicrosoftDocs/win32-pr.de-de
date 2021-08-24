---
description: Der Microsoft XPS Document Writer (MXDW) ist ein Drucker-zu-Datei-Treiber, der es einer Windows Anwendung ermöglicht, XML Paper Specification-Dokumentdateien (XPS) auf Versionen von Windows zu erstellen, die mit Windows XP mit Service Pack 2 (SP2) beginnen.
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Microsoft XPS Document Writer (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba69a6efff4f2da0ab0cc03bdc71468dada14c457de7685053096d2fba672d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938885"
---
# <a name="microsoft-xps-document-writer-mxdw"></a>Microsoft XPS Document Writer (MXDW)

Der Microsoft XPS Document Writer (MXDW) ist ein Drucker-zu-Datei-Treiber, der es einer Windows Anwendung ermöglicht, XML Paper Specification-Dokumentdateien (XPS) auf Versionen von Windows zu erstellen, die mit Windows XP mit Service Pack 2 (SP2) beginnen. Die Verwendung von MXDW ermöglicht es einer Windows Anwendung, ihren Inhalt als XPS-Dokument zu speichern, ohne den Programmcode der Anwendung zu ändern.

## <a name="when-to-use"></a>Verwendungs wann

Als Benutzer würden Sie das MXDW auswählen, wenn Sie ein XPS-Dokument aus einer Windows Anwendung erstellen möchten, die nicht die Möglichkeit hat, den Inhalt als XPS-Dokument zu speichern.

Als Anwendungsentwickler würden Sie das MXDW benutzern empfehlen, die XPS-Dokumente erstellen möchten, wenn Ihre Anwendung nicht die Option zum Speichern als XPS-Dokument anbietet. Weitere Informationen zu den XML Paper Specification- und XPS-Dokumenten finden Sie unter [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) und [XPS-Spezifikation und Lizenzdownloads.](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)

MxDW wird automatisch auf Windows Vista und neueren Versionen von Windows installiert und kann auf Windows XP mit SP2 und Windows Server 2003 heruntergeladen und installiert werden.

## <a name="installation"></a>Installation

Auf Windows Vista und neueren Versionen von Windows wird das MXDW automatisch installiert, wenn das Betriebssystem installiert wird.

**Windows XP mit SP2 und Windows Server 2003:** Laden Sie .NET Framework 3.0 oder das XPS Essential Pack aus dem [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx)herunter, und installieren Sie es.

## <a name="how-to-use"></a>Verwendung

Nach der Installation wird mxdw als verfügbare Druckwarteschlange im Dialogfeld Drucken angezeigt, das von einer Anwendung angezeigt wird. Wenn mxdw als Drucker ausgewählt ist, wird der Benutzer aufgefordert, den Dateinamen als XPS-Dokument zu erstellen, das die Druckausgabe der Anwendung erfasst.

Die folgende Abbildung zeigt das MXDW, das im allgemeinen Druckdialogfeld Windows Vista als Drucker ausgewählt wird.

![Abbildung des Druckdialogfelds, das die Auswahl des Microsoft XPS-Dokumentwriters (mxdw) anzeigt](images/choosingmxdwinvista.gif)

Anwendungsentwickler können die Ausgabe von MXDW mithilfe der [MXDW-Konfigurationseinstellungen](mxdw-configuration-settings.md)anpassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[XPS-Spezifikation und Lizenzdownloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[isXPS Conformance Tool](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))
</dt> <dt>

[MXDW-Konfigurationseinstellungen](mxdw-configuration-settings.md)
</dt> </dl>

 

 
