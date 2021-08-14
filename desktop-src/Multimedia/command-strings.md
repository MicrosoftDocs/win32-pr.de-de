---
title: Befehlszeichenfolgen
description: Befehlszeichenfolgen
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- MCI-Befehlszeichenfolgen, Informationen
- MCI-Befehlszeichenfolgen, Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f3638271dd004db13fe3ee2f0517eef0c1d2fe72be93da37a73f47e6666212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807830"
---
# <a name="command-strings"></a>Befehlszeichenfolgen

Um einen Zeichenfolgenbefehl an ein MCI-Gerät zu senden, verwenden Sie die [**mciSendString-Funktion,**](/previous-versions//dd757161(v=vs.85)) die Parameter für den Zeichenfolgenbefehl und einen Puffer für alle zurückgegebenen Informationen enthält.

Die **mciSendString-Funktion gibt** bei Erfolg 0 (null) zurück. Wenn die Funktion fehlschlägt, enthält das niedrige Wort des Rückgabewerts einen Fehlercode. Sie können diesen Fehlercode an die [**mciGetErrorString-Funktion**](/previous-versions//dd757158(v=vs.85)) übergeben, um eine Textbeschreibung des Fehlers zu erhalten.

## <a name="syntax-of-command-strings"></a>Syntax von Befehlszeichenfolgen

MCI-Befehlszeichenfolgen verwenden eine konsistente Syntax für verb-object-modifier. Jede Befehlszeichenfolge enthält einen Befehl, eine Geräte-ID und Befehlsargumente. Argumente sind für einige Befehle optional und für andere erforderlich.

Eine Befehlszeichenfolge hat das folgende Formular:

*\_Befehlsgeräte-ID-Argumente*

Diese Komponenten enthalten die folgenden Informationen:

-   Der *Befehl* gibt einen MCI-Befehl an, z. B. [**öffnen,**](open.md) [**schließen**](close.md)oder [**wiedergibt.**](play.md)
-   Die *\_ Geräte-ID* identifiziert eine Instanz eines MCI-Treibers. Die *\_ Geräte-ID* wird erstellt, wenn das Gerät geöffnet wird.
-   Die *Argumente* geben die Flags und Variablen an, die vom Befehl verwendet werden. Flags sind Schlüsselwörter, die mit dem MCI-Befehl erkannt werden. Variablen sind Zahlen oder Zeichenfolgen, die für den MCI-Befehl oder das MCI-Flag gelten.

    Beispielsweise verwendet der **Play-Befehl** die Argumente "from *position"* und "to *position",* um die Positionen anzugeben, an denen die Wiedergabe gestartet und beendet werden soll. Sie können die mit einem Befehl verwendeten Flags in beliebiger Reihenfolge auflisten. Wenn Sie ein Flag verwenden, dem eine Variable zugeordnet ist, müssen Sie einen Wert für die Variable geben.

    Nicht angegebene (und optionale) Befehlsargumente setzen einen Standardwert voraus.

Die folgende Beispielfunktion sendet den [**Play-Befehl**](play.md) mit den Flags "from" und "to".


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



## <a name="data-types-for-command-variables"></a>Datentypen für Befehlsvariablen

Sie können die folgenden Datentypen für die Variablen in einer Befehlszeichenfolge verwenden.



| **Datentyp**        | **Beschreibung**                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zeichenfolgen              | Zeichenfolgendatentypen werden durch führende und nachstellende Leerzeichen und Anführungszeichen getrennt. MCI entfernt einfache Anführungszeichen aus einer Zeichenfolge. Um ein Anführungszeichen in eine Zeichenfolge zu setzen, verwenden Sie einen Satz von zwei Anführungszeichen, in die Sie Das Anführungszeichen einbetten möchten. Um eine leere Zeichenfolge zu verwenden, verwenden Sie zwei Anführungszeichen, die durch führende und nachstehende Leerzeichen getrennt sind. |
| Lange ganze Zahlen mit Vorzeichen | Datentypen mit langen ganzen Zahlen mit Vorzeichen werden durch führende und nachstellende Leerzeichen getrennt. Sofern nicht anders angegeben, können ganze Zahlen positiv oder negativ sein. Wenn Sie negative ganze Zahlen verwenden, sollten Sie das Minuszeichen und die erste Ziffer nicht durch ein Leerzeichen trennen.                                                                                                    |
| Rechtecke           | Rechteckdatentypen sind eine geordnete Liste mit vier kurz signierten Werten. Leerraum begrenzt diesen Datentyp und trennt jede ganze Zahl in der Liste.                                                                                                                                                                                                              |



 

 

 