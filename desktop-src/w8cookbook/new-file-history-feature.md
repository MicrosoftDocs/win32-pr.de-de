---
title: Neues Dateiversionsverlauf feature
description: Neues Dateiversionsverlauf feature
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1502450c1376a57f9de99badc5188c8ce07761e0c28ae3ac2245a84437b5e66d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932190"
---
# <a name="new-file-history-feature"></a>Neues Dateiversionsverlauf feature

## <a name="platform"></a>Plattform

**Clients** – Windows 8 


## <a name="description"></a>Beschreibung

Das neue Dateiversionsverlauf ersetzt die vorhandene Sicherungs- und Wiederherstellungsfunktion und bietet Schutz für Benutzerdateien, die in Benutzerbibliotheken gespeichert sind. Es wird eine Reihe von APIs bereitgestellt, mit denen Entwickler programmgesteuert Dateiversionsverlauf und ein bestimmtes Speicherziel auswählen können. Die Dokumentation für diese APIs ist auf MSDN verfügbar.

Dies kann sich auf Workflows im Zusammenhang mit dem Datenschutz und der Dokumentation auswirken, die von der Windows-Sicherung- und Wiederherstellungsfunktion abhängen.

Es wird nicht empfohlen, beide Features gleichzeitig zu verwenden. Dateiversionsverlauf überprüft, ob ein Sicherungszeitplan vorhanden und aktiv ist, und wenn er einen findet, können Benutzer ihn nicht aktivieren. In diesem Fall müssen Benutzer, die Dateiversionsverlauf möchten, den Zeitplan Windows-Sicherung löschen.

## <a name="manifestation"></a>Manifestation

Workflows können unterbrochen werden, und die Dokumentation für die vorherige Methode für den Zugriff auf die Windows-Sicherung und das Wiederherstellungsfeature müssen aktualisiert werden, um diese Änderungen widerzuentigen.

## <a name="solution"></a>Lösung

Überarbeiten Sie Apps, die Workflows enthalten, die durch das neue Dateiversionsverlauf-Feature beeinträchtigt werden, um Konflikte zu entfernen und den neuen Satz von APIs zu integrieren.

## <a name="tests"></a>Tests

Mit der API können Entwickler ermitteln, ob Dateiversionsverlauf aktiviert ist.

 

 




