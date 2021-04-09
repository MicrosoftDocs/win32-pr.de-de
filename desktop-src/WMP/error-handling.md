---
title: Fehlerbehandlung (Windows Media Player SDK)
description: Fehlerbehandlung
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Windows Media Player, Fehlerbehandlung
- Windows Media Player-Objektmodell, Fehlerbehandlung
- Objektmodell, Fehlerbehandlung
- Windows Media Player ActiveX-Steuerelement, Fehlerbehandlung
- ActiveX-Steuerelement, Fehlerbehandlung
- Windows Media Player Mobile ActiveX-Steuerelement, Fehlerbehandlung
- Windows Media Player Mobile, Fehlerbehandlung
- Migrations Handbuch, Fehlerbehandlung
- Fehlerbehandlung im Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102626"
---
# <a name="error-handling-windows-media-player-sdk"></a>Fehlerbehandlung (Windows Media Player SDK)

Das ActiveX-Steuerelement von Windows Media Player 6,4 bietet eine standardmäßige Fehlerbehandlung, indem Fehlermeldungen in Dialogfeldern und in der Statusleiste angezeigt werden. Sie können auch eine benutzerdefinierte Fehlerbehandlung bereitstellen, indem Sie Fehler in Ihrem Skript verarbeiten. Die Fehlerbehandlung erfolgt durch ereignisgesteuert. Dies bedeutet, dass Sie für jeden Fehler eine Benachrichtigung erhalten, und Sie müssen entscheiden, wie die einzelnen Fehlerereignisse behandelt werden sollen, wenn Sie auftreten. Weitere Informationen zur Behandlung von Fehlern mit dem Objektmodell der Version 6,4 finden Sie im Abschnitt zur Fehlerbehandlung im Handbuch zu Version 6,4 Player-Objekt Modellen, der Teil des Windows Media Player SDK ist.

Das Objektmodell Windows Media Player 7 oder höher stellt das **Fehler** Objekt und das **ErrorItem** -Objekt bereit, um Fehler zu behandeln. Diese beiden Objekte arbeiten zusammen, um Ihnen einen Fehler Behandlungs Mechanismus bereitzustellen, mit dem Sie den Fehler Behandlungsprozess vervollständigen und flexibel steuern können. Das **Error** -Objekt ermöglicht den Zugriff auf eine Auflistung von **ErrorItem** -Objekten. Jedes **ErrorItem** -Objekt stellt Details zu einer einzelnen Fehlermeldung bereit.

Wenn ein Fehler auftritt, werden die Fehlerinformationen an eine Fehler Warteschlange gesendet. Die Warteschlange ist eine Sammlung von **ErrorItem** -Objekten. Jeder Fehler, der der Warteschlange hinzugefügt wird, ist einer Indexnummer (beginnend mit null) zugeordnet, die zum Identifizieren des jeweiligen **ErrorItem** -Objekts verwendet werden kann. Der *Fehler*. die **errorCount** -Eigenschaft ruft die Anzahl der Fehler in der Fehler Warteschlange ab. Da die Indexnummern Null basiert sind, weist der letzte Fehler, der an die Warteschlange gesendet wird, immer einen Indexwert auf, der " *Error*" entspricht. **errorCount** minus 1.

Sie können einen Fehler Ereignishandler für Windows-Media Player mithilfe eines Skripts erstellen. Im folgenden JScript-Beispiel wird gezeigt, wie das letzte Fehler Element aus der Fehler Warteschlange abgerufen und der Fehlercode und die Fehlerbeschreibung mithilfe des Objektmodells Windows Media Player 7 oder höher angezeigt werden. Das **Player** -Objekt wurde mit ID = "WMP9" erstellt.


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



Das **Error** -Objekt verfügt über zwei zusätzliche Methoden, die Sie verwenden können. Der *Fehler*. mit der **clearerrorqueue** -Methode können Sie alle Fehler aus der Fehler Warteschlange entfernen und die Indexnummer auf Null zurücksetzen. Sie haben die komplette Kontrolle über diesen Prozess. Sie können Fehler in der Warteschlange so lange beibehalten, wie Sie verfügbar sein müssen, und dann die Warteschlange leeren, wenn Sie die Fehlerbehandlung abgeschlossen haben.

Der *Fehler*. die **WebHelp** -Methode bietet eine Möglichkeit, dem Benutzer die aktuellsten Fehlerinformationen über das Internet anzuzeigen. Beim Aufrufen überträgt diese Methode alle relevanten Informationen zum ersten Fehler in der Warteschlange (der mit dem Index 0 (null)) an die Microsoft Windows Media Player-Webhilfe, die weitere Informationen über den Fehler im aktuellen Browserfenster anzeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Error-Objekt**](error-object.md)
</dt> <dt>

[**ErrorItem-Objekt**](erroritem-object.md)
</dt> <dt>

[**Handbuch für die Migration des Objektmodells**](object-model-migration-guide.md)
</dt> </dl>

 

 




