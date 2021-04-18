---
description: 'Jeder Prozess verfügt über einen Umgebungsblock, der einen Satz von Umgebungsvariablen und deren Werte enthält. Es gibt zwei Arten von Umgebungsvariablen: Benutzer Umgebungsvariablen (für jeden Benutzer festgelegt) und System Umgebungsvariablen (für alle festgelegt).'
ms.assetid: 6732b12f-ced1-4769-b947-79da8fd2237a
title: Umgebungsvariablen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f50226d12286d01c77025d1cc38e33e2778392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348007"
---
# <a name="environment-variables"></a>Umgebungsvariablen

Jeder Prozess verfügt über einen Umgebungsblock, der einen Satz von Umgebungsvariablen und deren Werte enthält. Es gibt zwei Arten von Umgebungsvariablen: Benutzer Umgebungsvariablen (für jeden Benutzer festgelegt) und System Umgebungsvariablen (für alle festgelegt).

Standardmäßig erbt ein untergeordneter Prozess die Umgebungsvariablen des übergeordneten Prozesses. Programme, die vom Befehlsprozessor gestartet werden, erben die Umgebungsvariablen des Befehls Prozessors. Wenn Sie eine andere Umgebung für einen untergeordneten Prozess angeben möchten, erstellen Sie einen neuen Umgebungsblock, und übergeben Sie einen Zeiger als Parameter an die Funktion "up- [**Process**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ".

Der Befehlsprozessor stellt den **Set** -Befehl bereit, um den Umgebungsblock anzuzeigen oder neue Umgebungsvariablen zu erstellen. Sie können die Umgebungsvariablen auch anzeigen oder ändern, indem Sie in der System **Steuerung** die Option **System** auswählen, **Erweiterte System Einstellungen** auswählen und auf **Umgebungsvariablen** klicken.

Jeder Umgebungsblock enthält die Umgebungsvariablen im folgenden Format:<dl> *Var1* = *Value1* \\ 1,0  
*Var2* = *Value2* \\ 1,0  
*Var3* = *Wert3* \\ 1,0  
...  
*Varn* = *ValueN* \\ 0 \\ 0  
</dl>

Der Name einer Umgebungsvariablen darf kein Gleichheitszeichen (=) enthalten.

Die [**getenvironmentstrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) -Funktion gibt einen Zeiger auf den Umgebungsblock des aufrufenden Prozesses zurück. Dies sollte als Schreib geschützter Block behandelt werden. Ändern Sie ihn nicht direkt. Verwenden Sie stattdessen die Funktion " [**settenvironmentvariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) ", um eine Umgebungsvariable zu ändern. Wenn Sie den Umgebungsblock, der von **getenvironmentstrings** abgerufen wurde, fertiggestellt haben, können Sie die [**freeenvironment Strings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa) -Funktion aufrufen, um den Block freizugeben.

Der Aufruf von " [**settenvironmentvariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) " hat keine Auswirkung auf die System Umgebungsvariablen. Um System Umgebungsvariablen Programm gesteuert hinzuzufügen oder zu ändern, fügen Sie Sie dem **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ Environment** Registry Key hinzu, und senden Sie dann eine [**WM \_ settingchange**](/windows/desktop/winmsg/wm-settingchange) -Nachricht mit *LPARAM* , die auf die Zeichenfolge "Environment" festgelegt ist. Dadurch können Anwendungen, wie z. b. die Shell, Ihre Updates abrufen.

Die maximale Größe einer benutzerdefinierten Umgebungsvariablen beträgt 32.767 Zeichen. Es gibt keine technische Einschränkung hinsichtlich der Größe des Umgebungs Blocks. Abhängig von dem Mechanismus, der für den Zugriff auf den Block verwendet wird, gibt es jedoch praktische Einschränkungen. Beispielsweise kann eine Batchdatei keine Variable festlegen, die länger als die maximale Befehlszeilen Länge ist.

**Windows Server 2003 und Windows XP:** Die maximale Größe des Umgebungs Blocks für den Prozess beträgt 32.767 Zeichen. Ab Windows Vista und Windows Server 2008 gibt es keine technische Einschränkung hinsichtlich der Größe des Umgebungs Blocks.

Die [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable) -Funktion bestimmt, ob eine angegebene Variable in der Umgebung des aufrufenden Prozesses definiert ist, und wenn dies der Fall ist, was der Wert ist.

Verwenden Sie die Funktion " [**kreateenvironment Block**](/windows/win32/api/userenv/nf-userenv-createenvironmentblock) ", um eine Kopie des Umgebungs Blocks für einen bestimmten Benutzer abzurufen.

Um Umgebungsvariablen-Zeichen folgen zu erweitern, verwenden Sie die [**expandenvironment Strings**](/windows/desktop/api/processenv/nf-processenv-expandenvironmentstringsa) -Funktion.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ändern von Umgebungsvariablen](changing-environment-variables.md)
</dt> <dt>

[Benutzer Umgebungsvariablen](../shell/user-environment-variables.md)
</dt> </dl>

 

 
