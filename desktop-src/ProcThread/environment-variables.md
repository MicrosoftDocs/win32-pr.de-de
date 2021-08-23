---
description: 'Jeder Prozess verfügt über einen Umgebungsblock, der eine Reihe von Umgebungsvariablen und deren Werte enthält. Es gibt zwei Arten von Umgebungsvariablen: Benutzerumgebungsvariablen (für jeden Benutzer festgelegt) und Systemumgebungsvariablen (für alle Benutzer festgelegt).'
ms.assetid: 6732b12f-ced1-4769-b947-79da8fd2237a
title: Umgebungsvariablen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647c685aac8ed6df36c0312d7eef49793fd4b2bbfca5576e0377e59da31dd777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910320"
---
# <a name="environment-variables"></a>Umgebungsvariablen

Jeder Prozess verfügt über einen Umgebungsblock, der eine Reihe von Umgebungsvariablen und deren Werte enthält. Es gibt zwei Arten von Umgebungsvariablen: Benutzerumgebungsvariablen (für jeden Benutzer festgelegt) und Systemumgebungsvariablen (für alle Benutzer festgelegt).

Standardmäßig erbt ein untergeordneter Prozess die Umgebungsvariablen seines übergeordneten Prozesses. Programme, die vom Befehlsprozessor gestartet werden, erben die Umgebungsvariablen des Befehlsprozessors. Um eine andere Umgebung für einen untergeordneten Prozess anzugeben, erstellen Sie einen neuen Umgebungsblock und übergeben einen Zeiger darauf als Parameter an die [**CreateProcess-Funktion.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)

Der Befehlsprozessor stellt den **Befehl set** zum Anzeigen des Umgebungsblocks oder zum Erstellen neuer Umgebungsvariablen zur Seite. Sie können die Umgebungsvariablen auch  anzeigen oder ändern, indem Sie im Systemsteuerung die Option System **auswählen,** Erweiterte Systemeinstellungen auswählen und auf **Umgebungsvariablen klicken.**

Jeder Umgebungsblock enthält die Umgebungsvariablen im folgenden Format:<dl> *Var1* = *Wert1* \\ 0  
*Var2* = *Value2* \\ 0  
*Var3* = *Wert3* \\ 0  
...  
*VarN* = *ValueN* \\ 0 \\ 0  
</dl>

Der Name einer Umgebungsvariablen darf kein Gleichheitszeichen (=) enthalten.

Die [**GetEnvironmentStrings-Funktion**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) gibt einen Zeiger auf den Umgebungsblock des aufrufenden Prozesses zurück. Dies sollte als schreibgeschützter Block behandelt werden. ändern Sie sie nicht direkt. Verwenden Sie stattdessen die [**SetEnvironmentVariable-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) um eine Umgebungsvariable zu ändern. Wenn Sie mit dem Umgebungsblock fertig sind, der von **GetEnvironmentStrings** erhalten wurde, rufen Sie die [**FreeEnvironmentStrings-Funktion**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa) auf, um den Block frei zu geben.

Das [**Aufrufen von SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) hat keine Auswirkungen auf die Systemumgebungsvariablen. Um Systemumgebungsvariablen programmgesteuert hinzuzufügen oder zu ändern, fügen Sie sie dem **Registrierungsschlüssel des HKEY \_ LOCAL MACHINE-Systems \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ Environment** hinzu, und senden Sie dann eine [**WM \_ SETTINGCHANGE-Nachricht,**](/windows/desktop/winmsg/wm-settingchange) bei der *lParam* auf die Zeichenfolge "Environment" festgelegt ist. Dadurch können Anwendungen, z. B. die Shell, Ihre Updates auswählen.

Die maximale Größe einer benutzerdefinierten Umgebungsvariablen beträgt 32.767 Zeichen. Es gibt keine technische Einschränkung für die Größe des Umgebungsblocks. Es gibt jedoch praktische Grenzwerte, die vom Mechanismus abhängen, der für den Zugriff auf den Block verwendet wird. Beispielsweise kann eine Batchdatei keine Variable festlegen, die länger als die maximale Befehlszeilenlänge ist.

**Windows Server 2003 und Windows XP:** Die maximale Größe des Umgebungsblocks für den Prozess beträgt 32.767 Zeichen. Ab Windows Vista und Windows Server 2008 gibt es keine technische Einschränkung für die Größe des Umgebungsblocks.

Die [**GetEnvironmentVariable-Funktion**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable) bestimmt, ob eine angegebene Variable in der Umgebung des aufrufenden Prozesses definiert ist und, falls ja, wie ihr Wert ist.

Um eine Kopie des Umgebungsblocks für einen bestimmten Benutzer abzurufen, verwenden Sie die [**CreateEnvironmentBlock-Funktion.**](/windows/win32/api/userenv/nf-userenv-createenvironmentblock)

Verwenden Sie die Funktion [**ExpandEnvironmentStrings, um Umgebungsvariablenzeichenfolgen zu**](/windows/desktop/api/processenv/nf-processenv-expandenvironmentstringsa) erweitern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ändern von Umgebungsvariablen](changing-environment-variables.md)
</dt> <dt>

[Benutzerumgebungsvariablen](../shell/user-environment-variables.md)
</dt> </dl>

 

 
