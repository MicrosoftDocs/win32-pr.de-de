---
title: Verwenden von Anwendungs Wiederherstellung und Neustart
description: Eine Anwendung kann die Anwendungs Wiederherstellung und den Neustart (arr) verwenden, um Daten und Zustandsinformationen zu speichern, bevor die Anwendung aufgrund einer nicht behandelten Ausnahme beendet wird, oder wenn die Anwendung nicht mehr reagiert. Die Anwendung wird bei Bedarf ebenfalls neu gestartet.
ms.assetid: 28cbb4c0-a287-4302-b3a9-daddc69adb40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5bf0b9bd0e0f6cc257ee785ab5df6febc8fef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858290"
---
# <a name="using-application-recovery-and-restart"></a>Verwenden von Anwendungs Wiederherstellung und Neustart

Eine Anwendung kann die Anwendungs Wiederherstellung und den Neustart (arr) verwenden, um Daten und Zustandsinformationen zu speichern, bevor die Anwendung aufgrund einer nicht behandelten Ausnahme beendet wird, oder wenn die Anwendung nicht mehr reagiert. Die Anwendung wird bei Bedarf ebenfalls neu gestartet.

Wenn Sie sich für die Wiederherstellung oder den Neustart registrieren, werden die Registrierungsinformationen dem Prozess hinzugefügt. [Windows-Fehlerberichterstattung (wer)](/windows/desktop/wer/windows-error-reporting) verwendet die Registrierungsinformationen, um den Wiederherstellungs Rückruf aufzurufen und die Anwendung neu zu starten. Wenn Sie sich z. b. für die Wiederherstellung registrieren und die Anwendung auf eine nicht behandelte Ausnahme stößt, zeigt wer einen Dialog für den Benutzer an, der dem Benutzer die Möglichkeit gibt, eine Projekt Mappe online zu überprüfen, das Programm zu schließen oder das Programm zu debuggen. Wenn der Benutzer eine Prüfung auf eine Projekt Mappe durchführt oder das Programm schließt, ruft wer den registrierten Rückruf auf und gibt der Anwendung die Möglichkeit, Daten und Zustandsinformationen zu speichern. Wenn die Wiederherstellung abgeschlossen ist, wird die Anwendung beendet.

Wenn Sie sich für den Neustart registrieren und die Anwendung auf eine nicht behandelte Ausnahme stößt, zeigt wer dem Benutzer das gleiche Dialogfeld an, bietet jedoch die Möglichkeit, das Programm neu zu starten, statt das Programm zu schließen. Wenn Sie sich für die Wiederherstellung und den Neustart registrieren, erfolgt die Wiederherstellung zuerst. die Anwendung wird dann beendet und neu gestartet.

Eine nicht reagierende Anwendung wird auf ähnliche Weise behandelt. Eine Anwendung gilt als nicht reagierend, wenn Sie fünf Sekunden lang nicht auf Windows-Meldungen antwortet und der Benutzer dann versucht, mit der Anwendung zu interagieren. der Benutzer wird in der Titelleiste angezeigt (antwortet nicht). Wer wird aktiviert, wenn der Benutzer auf die Schaltfläche zum Schließen des Systems klickt.

Sie müssen sich für die Wiederherstellung registrieren oder den Neustart oder die Registrierung aufheben, bevor die Anwendung nicht mehr reagiert oder eine nicht behandelte Ausnahme feststellt. In Ihrem Wiederherstellungs Rückruf können Sie jedoch die Befehlszeile für den Neustart ändern.

Weitere Informationen zum Registrieren für die Wiederherstellung oder zum Neustart finden Sie in den folgenden Themen:

-   [Registrieren für die Anwendungs Wiederherstellung](registering-for-application-recovery.md)
-   [Registrieren für Anwendungs Neustart](registering-for-application-restart.md)

Beispiele, in denen die Wiederherstellungs-und Neustart Features implementiert werden, finden Sie in den Beispielen apprecovery und apprestart in der Windows SDK, die sich im Winbase \\ windowserrorreporting-Ordner befinden.

 

 