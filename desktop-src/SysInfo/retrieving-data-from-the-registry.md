---
description: Um Daten aus der Registrierung abzurufen, listet eine Anwendung in der Regel die Unterschlüssel eines Schlüssels auf, bis ein bestimmter Schlüssel gefunden wird, und ruft dann Daten aus dem oder den zugeordneten Werten ab.
ms.assetid: ce4be388-5506-4d01-a73c-33372ef4ccd7
title: Abrufen von Daten aus der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bedbe0631015188a8a9fe280ba17d929c83663e995f440f4528c0913fc69cb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763479"
---
# <a name="retrieving-data-from-the-registry"></a>Abrufen von Daten aus der Registrierung

Um Daten aus der Registrierung abzurufen, listet eine Anwendung in der Regel die Unterschlüssel eines Schlüssels auf, bis ein bestimmter Schlüssel gefunden wird, und ruft dann Daten aus dem oder den zugeordneten Werten ab. Eine Anwendung kann die [**RegEnumKeyEx-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa) aufrufen, um die Unterschlüssel eines bestimmten Schlüssels aufzuzählen.

Um detaillierte Daten zu einem bestimmten Unterschlüssel abzurufen, kann eine Anwendung die [**RegQueryInfoKey-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya) aufrufen. Die [**RegGetKeySecurity-Funktion**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity) ruft eine Kopie des Sicherheitsdeskriptors ab, der einen Schlüssel schützt.

Eine Anwendung kann die [**RegEnumValue-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) verwenden, um die Werte für einen bestimmten Schlüssel aufzuzählen, und die [**RegQueryValueEx-Funktion,**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) um einen bestimmten Wert für einen Schlüssel abzurufen. Eine Anwendung ruft in der Regel **RegEnumValue** auf, um die Wertnamen zu bestimmen, und dann **RegQueryValueEx,** um die Daten für die Namen abzurufen.

Die [**RegQueryMultipleValues-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa) ruft den Typ und die Daten für eine Liste von Wertnamen ab, die einem geöffneten Registrierungsschlüssel zugeordnet sind. Diese Funktion ist für dynamische Schlüsselanbieter nützlich, da sie die Konsistenz der Daten gewährleistet, indem mehrere Werte in einem atomaren Vorgang abgerufen werden.

Da andere Anwendungen die Daten in einem Registrierungswert zwischen dem Zeitpunkt ändern können, zu dem Ihre Anwendung einen Wert lesen und verwenden kann, müssen Sie möglicherweise sicherstellen, dass Ihre Anwendung über die neuesten Daten verfügt. Sie können die [**RegNotifyChangeKeyValue-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) verwenden, um den aufrufenden Thread zu benachrichtigen, wenn Änderungen an den Attributen oder Inhalten eines Registrierungsschlüssels vorgenommen werden oder der Schlüssel gelöscht wird. Die Funktion signalisiert einem Ereignisobjekt, dass der Aufrufer benachrichtigt wird. Wenn der Thread, der **RegNotifyChangeKeyValue** aufruft, beendet wird, wird das Ereignis signalisiert, und die Überwachung des Registrierungsschlüssels wird beendet.

Sie können steuern oder angeben, welche Änderungen mithilfe eines Benachrichtigungsfilters oder -flags gemeldet werden sollen. In der Regel werden Änderungen gemeldet, indem ein Ereignis signalisiert wird, das Sie für die Funktion angeben. Beachten Sie, dass die [**RegNotifyChangeKeyValue-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) nicht mit Remotehandles funktioniert.

Ausführlichere Informationen zum Überwachen von Registrierungsvorgängen finden Sie unter [**Registrierung**](/windows/desktop/ETW/registry).

 

 
