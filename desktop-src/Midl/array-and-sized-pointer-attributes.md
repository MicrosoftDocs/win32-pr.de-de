---
title: Array-und Sized-Pointer Attribute
description: Die Mittel Menge bietet einen umfangreichen Satz von Funktionen für die Übergabe von Daten Arrays und Zeiger auf Daten. Mit diesen Attributen können Sie Merkmale von Arrays und mehrere Zeiger Ebenen angeben.
ms.assetid: 482be83f-eb09-40a0-8dd6-a0cbf5dc4485
keywords:
- IDL-Mittell, Attribute, Array und Größen Zeiger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f9ba435d5c413ea152c2bc9b492486ccc1be94
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858203"
---
# <a name="array-and-sized-pointer-attributes"></a>Array-und Sized-Pointer Attribute

Die Mittel Menge bietet einen umfangreichen Satz von Funktionen für die Übergabe von Daten Arrays und Zeiger auf Daten. Mit diesen Attributen können Sie Merkmale von Arrays und mehrere Zeiger Ebenen angeben.



| Attribut                       | Verbrauch                                                                                                                                                                                                |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Größe \_ :**](size-is.md)     | Gibt den Umfang des Arbeitsspeichers an, der für Größen Zeiger, Größen Zeiger auf Größen Zeiger und einzelne oder mehrdimensionale Arrays zugeordnet werden soll.                                                         |
| [**Max \_ ist**](max-is.md)       | Der maximale Wert für einen Array Index.                                                                                                                                                                |
| [**Länge \_ ist**](length-is.md) | Die Anzahl der zu übertragenden Array Elemente.                                                                                                                                                      |
| [**der erste \_ ist**](first-is.md)   | Der Index des ersten Array Elements, das übertragen werden soll.                                                                                                                                              |
| [**Letzter \_ ist**](last-is.md)     | Gibt den Index des letzten Array Elements an, das übertragen werden soll.                                                                                                                                         |
| [**Zeichenfolge**](string.md)        | Gibt an, dass das eindimensionale [**char**](char-idl.md)-, [**WCHAR \_ t**](wchar-t.md)-, [**Bytearray**](byte.md) -Array oder der-Zeiger auf ein solches Array als Zeichenfolge behandelt werden soll. |
| [**Bereich**](range.md)          | Gibt einen Bereich zulässiger Werte für Argumente oder Felder an, deren Werte zur Laufzeit festgelegt werden.                                                                                                       |



 

"Mittel l" unterstützt drei Arten von Zeigern: Verweis Zeiger, eindeutige Zeiger und vollständige Zeiger. Diese Zeiger werden durch die Zeiger Attribute [**ref**](ref.md), [**Unique**](unique.md)und [**ptr**](ptr.md)angegeben.

Ein Zeiger Attribut kann als Type-Attribut angewendet werden. als Feld Attribut, das für einen Strukturmember, ein Union-Member oder einen-Parameter gilt. oder als Funktions Attribut, das für den Funktions Rückgabetyp gilt. Das Zeiger Attribut kann auch mit dem [**Zeiger \_ default**](pointer-default.md) -Schlüsselwort angezeigt werden.

Damit ein Zeiger Parameter während einer Remote Funktion den Wert ändern kann, müssen Sie eine andere Dereferenzierungsebene bereitstellen, indem Sie mehrere Zeiger Deklaratoren bereitstellen. Das explizite Zeiger Attribut, das auf den-Parameter angewendet wird, wirkt sich nur auf den ganz rechts zeigerdeklarator für den Parameter aus Wenn mehrere Zeiger Deklaratoren in einer Parameter Deklaration vorhanden sind, werden die anderen Deklaratoren standardmäßig auf das vom [**Zeiger- \_ Standard**](pointer-default.md) Attribut angegebene Zeiger Attribut festgelegt. Wenn Sie unterschiedliche Zeiger Attribute auf mehrere Zeiger Deklaratoren anwenden möchten, müssen Sie zwischen Typen definieren, die die expliziten Zeiger Attribute angeben.

## <a name="default-pointer-attribute-values"></a>Standard Pointer-Attribute Werte

Wenn kein Zeiger Attribut mit einem Zeiger verknüpft ist, bei dem es sich um einen Parameter handelt, wird angenommen, dass es sich um einen [**ref**](ref.md) -Zeiger handelt.

Wenn kein Zeiger Attribut mit einem Zeiger verknüpft ist, der ein Member einer Struktur oder Union ist, weist der mittlerer l-Compiler Zeiger Attribute mithilfe der folgenden Prioritätsregeln zu (1 ist der höchste Wert):

1.  Explizit auf den Zeigertyp angewendete Attribute
2.  Explizit auf den Zeiger Parameter oder Member angewendete Attribute
3.  Das [**Zeiger \_ Standard**](pointer-default.md) Attribut in der IDL-Datei, die den Typ definiert.
4.  Das [**Zeiger \_ Standard**](pointer-default.md) Attribut in der IDL-Datei, die den Typ importiert.
5.  [**ptr**](ptr.md) (OSF-Modus); [**eindeutig**](unique.md) (Microsoft RPC-Standardmodus)

Wenn die IDL-Datei im Standardmodus kompiliert wird, können importierte Dateien Zeiger Attribute aus dem Importieren von Dateien erben. Diese Funktion ist nicht verfügbar, wenn Sie die Kompilierung mit dem/[**eines Zertifikats**](-osf.md) -Schalter durchsetzen. Weitere Informationen finden Sie unter [**Import**](import.md).

## <a name="function-return-types"></a>Funktions Rückgabe Typen

Ein Zeiger, der von einer Funktion zurückgegeben wird, muss ein eindeutiger Zeiger oder ein voll [**ständiger Zeiger sein**](unique.md) . Der mittlerer l-Compiler meldet einen Fehler, wenn ein Funktionsergebnis ein Verweis Zeiger ist, entweder explizit oder standardmäßig. Der zurückgegebene Zeiger gibt immer neuen Speicher an.

Funktionen, die einen Zeiger Wert zurückgeben, können ein Zeiger Attribut als Funktions Attribut angeben. Wenn ein Zeiger Attribut nicht vorhanden ist, verwendet der Funktionsergebnis Zeiger den Wert, der als [**Zeiger \_ Standard**](pointer-default.md) Attribut bereitgestellt wird.

## <a name="pointer-attributes-in-type-definitions"></a>Zeiger Attribute in Typdefinitionen

Wenn Sie ein Zeiger Attribut auf oberster Ebene einer [**typedef**](typedef.md) -Anweisung angeben, wird das angegebene Attribut wie erwartet auf den zeigerdeklarator angewendet. Wenn kein Zeiger Attribut angegeben wird, erben Zeiger Deklaratoren auf der obersten Ebene einer typedef-Anweisung bei Verwendung den Zeiger Attributtyp.

DCE IDL lässt nicht zu, dass das gleiche Zeiger Attribut zweimal explizit angewendet wird – z. b. in der [**typedef**](typedef.md) -Deklaration und in der Parameter Attribut Liste. Wenn Sie den Standardmodus (Microsoft Extensions) des compl-Compilers verwenden, wird diese Einschränkung gelockert.

Eine Erörterung der Verwendung von Mittel l-Arrays und Zeigern in Remote Prozedur aufrufen finden Sie unter [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).

 

 