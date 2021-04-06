---
description: Die Beispiel Programme in den folgenden Abschnitten führen Vorgänge aus, die erfordern, dass öffentliche/private Schlüsselpaare zum Verschlüsseln und Entschlüsseln von Dateien, Nachrichten und Signaturen verfügbar sind.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Erforderliche Schlüssel Container, Schlüssel und Zertifikate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759463"
---
# <a name="necessary-key-containers-keys-and-certificates"></a>Erforderliche Schlüssel Container, Schlüssel und Zertifikate

Die Beispiel Programme in den folgenden Abschnitten führen Vorgänge aus, die erfordern, dass [*öffentliche/private Schlüsselpaare*](../secgloss/p-gly.md) zum Verschlüsseln und Entschlüsseln von Dateien, Nachrichten und Signaturen verfügbar sind. Viele dieser Programme werden zur Laufzeit kompiliert, verknüpft und ausgeführt, schlagen aber fehl, ohne dass in diesen speichern ordnungsgemäße [*Schlüssel Container*](../secgloss/k-gly.md), Schlüssel, [*Zertifikat Speicher*](../secgloss/c-gly.md)und Zertifikate vorhanden sind.

Außerdem müssen einige der Zertifikate im My-Speicher einige erweiterte Eigenschaften haben.

Der erforderliche Standardschlüssel Container kann erstellt werden, indem das Programm im [Beispiel C-Programm: Erstellen eines Schlüssel Containers und Erstellen von Schlüsseln](example-c-program-creating-a-key-container-and-generating-keys.md)ausgeführt wird. Beachten Sie, dass bei der Erstellung eines Schlüssel Containers nicht automatisch öffentliche/private Schlüsselpaare generiert werden. Das Beispielprogramm erstellt jedoch den Schlüssel Container und generiert die Paare aus öffentlichem und privatem Schlüssel.

Nachdem öffentliche/private Schlüsselpaare generiert wurden, können Test Zertifikate, die diese Schlüssel verwenden, von einer [*Zertifizierungs*](../secgloss/c-gly.md) Stelle abgerufen werden.

Einige der Programme gehen davon aus, dass Zertifikate mit bestimmten Antragsteller Namen im eigenen Systemspeicher vorhanden sind. Insbesondere suchen mehrere Programme nach Zertifikaten mit den Antragsteller Namen "Full Test CERT" und "Hortense". Die Antragsteller Namen für die Zertifikate können im Code geändert werden, damit Sie mit den Antragsteller Namen von Zertifikaten identisch sind, die im My-Zertifikat Speicher vorhanden sind.

Durch Ausführen des Beispiel Programms im [Beispiel C-Programm: durch das Auflisten der Zertifikate in einem Speicher](example-c-program-listing-the-certificates-in-a-store.md) werden alle Zertifikate in einem Speicher und alle erweiterten Eigenschaften angezeigt, die für diese Zertifikate festgelegt sind.

 

 
