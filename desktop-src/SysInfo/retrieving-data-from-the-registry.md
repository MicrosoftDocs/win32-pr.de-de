---
description: Zum Abrufen von Daten aus der Registrierung listet eine Anwendung in der Regel die Unterschlüssel eines Schlüssels auf, bis eine bestimmte gefunden wird, und ruft dann Daten aus den zugeordneten Werten ab.
ms.assetid: ce4be388-5506-4d01-a73c-33372ef4ccd7
title: Abrufen von Daten aus der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d8dd6f6e4d667cf2760c7cba441200755fb6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050426"
---
# <a name="retrieving-data-from-the-registry"></a>Abrufen von Daten aus der Registrierung

Zum Abrufen von Daten aus der Registrierung listet eine Anwendung in der Regel die Unterschlüssel eines Schlüssels auf, bis eine bestimmte gefunden wird, und ruft dann Daten aus den zugeordneten Werten ab. Eine Anwendung kann die Funktion " [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa) " aufrufen, um die Unterschlüssel eines bestimmten Schlüssels aufzulisten.

Um ausführliche Daten zu einem bestimmten Unterschlüssel abzurufen, kann eine Anwendung die [**regqueryinfokey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya) -Funktion aufrufen. Die [**reggetkeysecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity) -Funktion Ruft eine Kopie der Sicherheits Beschreibung ab, die einen Schlüssel schützt.

Eine Anwendung kann mit der Funktion " [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) " die Werte für einen bestimmten Schlüssel auflisten und die Funktion " [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) " zum Abrufen eines bestimmten Werts für einen Schlüssel verwenden. Eine Anwendung ruft normalerweise " **regenenumvalue** " auf, um die Wertnamen zu ermitteln, und dann " **RegQueryValueEx** ", um die Daten für die Namen abzurufen.

Die [**regquerymultiplevalues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa) -Funktion Ruft den Typ und die Daten für eine Liste von Wert Namen ab, die einem geöffneten Registrierungsschlüssel zugeordnet sind. Diese Funktion ist für dynamische Schlüssel Anbieter nützlich, da Sie die Konsistenz der Daten gewährleistet, indem mehrere Werte in einer atomaren Operation abgerufen werden.

Da andere Anwendungen die Daten in einem Registrierungs Wert zwischen dem Zeitpunkt, an dem die Anwendung einen Wert lesen und verwenden kann, ändern können, müssen Sie möglicherweise sicherstellen, dass Ihre Anwendung über die neuesten Daten verfügt. Sie können die [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) -Funktion verwenden, um den aufrufenden Thread zu benachrichtigen, wenn Änderungen an den Attributen oder an den Inhalten eines Registrierungsschlüssels vorgenommen werden oder wenn der Schlüssel gelöscht wird. Die-Funktion signalisiert einem Ereignis Objekt, den Aufrufer zu benachrichtigen. Wenn der Thread, der **RegNotifyChangeKeyValue** aufruft, beendet wird, wird das Ereignis signalisiert, und die Überwachung des Registrierungsschlüssels wird beendet.

Sie können steuern oder angeben, welche Änderungen durch die Verwendung eines Benachrichtigungs Filters oder-Flags gemeldet werden sollen. Normalerweise werden Änderungen gemeldet, indem ein Ereignis signalisiert wird, das Sie für die Funktion angeben. Beachten Sie, dass die [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) -Funktion nicht mit Remote Handles funktioniert.

Weitere Informationen zum Überwachen von Registrierungs Vorgängen finden Sie unter [**Registrierung**](/windows/desktop/ETW/registry).

 

 
