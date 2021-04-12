---
title: Befehls Zeichenfolgen
description: Befehls Zeichenfolgen
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- MCI-Befehls Zeichenfolgen, Informationen zu
- MCI-Befehls Zeichenfolgen, Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390152"
---
# <a name="command-strings"></a>Befehls Zeichenfolgen

Um einen Zeichen folgen Befehl an ein MCI-Gerät zu senden, verwenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion, die Parameter für den Zeichen folgen Befehl und einen Puffer für alle zurückgegebenen Informationen enthält.

Die **mciSendString** -Funktion gibt bei Erfolg 0 zurück. Wenn die Funktion fehlschlägt, enthält das nieder wertige Wort des Rückgabewerts einen Fehlercode. Sie können diesen Fehlercode an die [**mcigeterrorstring**](/previous-versions//dd757158(v=vs.85)) -Funktion übergeben, um eine Textbeschreibung des Fehlers zu erhalten.

## <a name="syntax-of-command-strings"></a>Syntax von Befehls Zeichenfolgen

MCI-Befehls Zeichenfolgen verwenden eine konsistente Verb-Objekt-Modifier-Syntax. Jede Befehls Zeichenfolge enthält einen Befehl, einen Geräte Bezeichner und Befehlsargumente. Argumente sind für einige Befehle optional und für andere erforderlich.

Eine Befehls Zeichenfolge weist die folgende Form auf:

*Argumente der Befehls Geräte- \_ ID*

Diese Komponenten enthalten die folgenden Informationen:

-   Der *Befehl* gibt einen MCI-Befehl an, z. b. [**Öffnen**](open.md), [**Schließen**](close.md)oder [**abspielen**](play.md).
-   Die *Geräte- \_ ID* identifiziert eine Instanz eines MCI-Treibers. Die *Geräte- \_ ID* wird erstellt, wenn das Gerät geöffnet wird.
-   Die *Argumente* geben die Flags und Variablen an, die vom Befehl verwendet werden. Flags sind Schlüsselwörter, die mit dem MCI-Befehl erkannt werden. Variablen sind Zahlen oder Zeichen folgen, die auf den MCI-Befehl oder das Flag angewendet werden.

    Beispielsweise verwendet der **Wiedergabe** Befehl die Argumente "von *Position* " und "an *Position* ", um die Positionen anzugeben, an denen der Wiedergabe-und endwiedergabe angezeigt werden soll. Sie können die Flags auflisten, die mit einem Befehl in beliebiger Reihenfolge verwendet werden. Wenn Sie ein Flag verwenden, dem eine Variable zugeordnet ist, müssen Sie einen Wert für die Variable angeben.

    Nicht angegebene (und optionale) Befehlsargumente nehmen einen Standardwert an.

Die folgende Beispiel Funktion sendet den [**Wiedergabe**](play.md) Befehl mit den Flags "from" und "to".


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a>Datentypen für Befehls Variablen

Sie können die folgenden Datentypen für die Variablen in einer Befehls Zeichenfolge verwenden.



| **Datentyp**        | **Beschreibung**                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zeichenfolgen              | Zeichen folgen-Datentypen sind durch führende und nachfolgende Leerzeichen und Anführungszeichen begrenzt. MCI entfernt einfache Anführungszeichen aus einer Zeichenfolge. Wenn Sie ein Anführungszeichen in eine Zeichenfolge einfügen möchten, verwenden Sie einen Satz von zwei Anführungszeichen, in dem Sie das Anführungszeichen einbetten möchten. Um eine leere Zeichenfolge zu verwenden, verwenden Sie zwei Anführungszeichen, die durch führende und nachfolgende Leerzeichen getrennt sind. |
| Lange ganze Zahlen mit Vorzeichen | Datentypen für ganze Zahlen mit Vorzeichen sind durch führende und nachfolgende Leerzeichen begrenzt. Sofern nicht anders angegeben, können ganze Zahlen positiv oder negativ sein. Wenn Sie negative ganze Zahlen verwenden, sollten Sie das Minuszeichen und die erste Ziffer nicht durch ein Leerzeichen trennen.                                                                                                    |
| Rechtecke           | Rechteck Datentypen sind eine geordnete Liste von vier signierten kurzwerten. Leerraum begrenzt diesen Datentyp und trennt jede Ganzzahl in der Liste.                                                                                                                                                                                                              |



 

 

 