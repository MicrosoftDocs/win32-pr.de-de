---
title: partial_ignore-Attribut
description: Das ACF-Attribut \ partielle \_ Ignore \ definiert eine spezialisierte Version von \ Unique \-Zeigern, die eine optionale Semantik bereitstellt.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore Attribut-Mittel l
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82d133275ca77032341d160b51b95b20235c8f2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389280"
---
# <a name="partial_ignore-attribute"></a>partielles \_ Ignore-Attribut

Das ACF-Attribut **\[ partielle \_ Ignore \]** definiert eine **\[ \]** spezialisierte Version eindeutiger Zeiger, die eine optionale Semantik bereitstellt.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a>Bemerkungen

Beim Erstellen einer Funktion ist es üblich, Benutzern das Angeben eines nicht-**null** -Zeigers auf optionale Rückgabe Daten zu ermöglichen. Dies wird häufig als optionaler-out-Zeiger bezeichnet. Der Speicher, auf den der Benutzer zeigt, muss in der Regel nicht initialisiert werden. Diese Technik stellt ein Problem dar, wenn die Funktion über RPC verwendet wird.

Wenn der optionale-out-Zeiger gültig ist, aber auf nicht initialisierte Daten zeigt, versucht RPC, diese Daten zu Mars Hallen und an den Server zu senden, was dazu führen kann, dass das Marshalling fehlschlägt und den Aufruf abbricht. Auch wenn das Marshalling erfolgreich ist, wird eine potenziell große Menge an nutzlosen Daten an den Server gesendet.

Diese Probleme werden gelöst, indem der Zeiger als **\[ in, out, Unique, partiell \_ Ignore \]** gekennzeichnet wird. Alle vier Attribute müssen vorhanden sein. Wenn ein **\[ partieller \_ Ignore \]** -Zeiger auf der Clientseite gemarshallt wird, ist ein Indikator, der anzeigt, ob der Zeiger **null** ist. Wenn der Zeiger nicht **null** ist, empfängt die serverseitige Routine einen gültigen Zeiger auf einen Speicherblock, der mit Nullen initialisiert wurde. Wenn der Zeiger **null** ist, empfängt die serverseitige Routine einen **null** -Zeiger.

In dieser Situation muss die maximale Größe des Zeigers entweder zum Zeitpunkt der Kompilierung oder basierend auf den Eingabe Parametern festgelegt werden, da der Server Speicherplatz für den Speicherbereich zuweisen muss, auf den verwiesen wird. Ein einfacher **\[ Zeichen \]** folgen Zeiger hat z. b. keine klar definierte Größe, da die Zeichenfolge implizit mit einem NULL-Zeichen beendet wird. Wenn in diesem Fall die maximale Größe der Zeichenfolge durch Hinzufügen eines **\[ size \_ is \]** -Attributs angegeben wird, wird die genau definierte Größen Anforderung erreicht.

## <a name="examples"></a>Beispiele

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**gem**](unique.md)
</dt> </dl>

 

 




