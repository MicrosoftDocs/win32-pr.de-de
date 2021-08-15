---
title: partial_ignore-Attribut
description: Das ACF-Attribut \partial \_ ignore\ definiert eine spezielle Version von \unique\-Zeigern, die eine optionale Out-Semantik bereitstellt.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore-Attribut MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac751e5b3bdb4a93c003e170333af8956048c9793630419fff0857d61f8c1f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641973"
---
# <a name="partial_ignore-attribute"></a>\_Partielles Ignore-Attribut

Das **\[ partielle \_ Ignorieren \]** des ACF-Attributs definiert eine spezielle Version von **\[ eindeutigen \]** Zeigern, die eine optionale Out-Semantik bereitstellt.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a>Hinweise

Beim Erstellen einer Funktion ist es üblich, benutzern das Angeben eines Nicht-NULL-Zeigers auf optionale Rückgabedaten zu ermöglichen, die häufig als optionaler Out-Zeiger bezeichnet werden. Der Arbeitsspeicher, auf den der Benutzer zeigt, muss in der Regel nicht initialisiert werden. Diese Technik stellt ein Problem dar, wenn die Funktion über RPC verwendet wird.

Wenn der optionale Out-Zeiger gültig ist, aber auf nicht initialisierte Daten verweist, versucht RPC, diese Daten zu marshallen und an den Server zu senden. Dies kann dazu führen, dass das Marshalling fehlschlägt und den Aufruf abbricht. Auch wenn das Marshalling erfolgreich ist, wird eine potenziell große Menge von unbrauchbaren Daten an den Server gesendet.

Diese Probleme werden gelöst, indem der Zeiger als **\[ in, out, unique, partial \_ ignore \]** markiert wird. Alle vier Attribute müssen vorhanden sein. Wenn ein **\[ partieller \_ \] Ignore-Zeiger** auf clientseitiger Seite gemarshallt wird, sind die einzigen an den Server gesendeten Daten ein Indikator, der anzeigt, ob der Zeiger **NULL** ist. Wenn der Zeiger ungleich **NULL** ist, empfängt die serverseitige Routine einen gültigen Zeiger auf einen Speicherblock, der mit Nullen initialisiert wurde. Wenn der Zeiger **NULL** ist, empfängt die serverseitige Routine einen **NULL-Zeiger.**

In dieser Situation muss die maximale Größe des Zeigers entweder zur Kompilierzeit oder basierend auf Eingabeparametern klar definiert werden, da der Server Speicherplatz für den Speicherort zuweisen muss, auf den gezeigt wird. Beispielsweise hat ein einfacher **\[ \] Zeichenfolgenzeiger** keine klar definierte Größe, da die Zeichenfolge implizit durch ein NULL-Zeichen beendet wird. In diesem Fall würde die Angabe der maximalen Größe der Zeichenfolge durch Hinzufügen eines **\[ size \_ \] is-Attributs** die klar definierte Größenanforderung erfüllen.

## <a name="examples"></a>Beispiele

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Einzigartige**](unique.md)
</dt> </dl>

 

 




