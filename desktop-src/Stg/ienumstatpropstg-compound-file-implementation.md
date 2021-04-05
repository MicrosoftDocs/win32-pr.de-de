---
title: Implementierung der IEnumSTATPROPSTG-Compound Datei
description: Die Implementierung der Verbund Datei der ienumstatus propstg-Schnittstelle wird zum Auflisten von Eigenschaften verwendet. Dies führt zu Status Werten, die statistische Eigenschaften Daten enthalten.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- Ienumstatus propstg-Schnittstellen-Erweiterung, Implementierung von Verbund Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949015"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a>Implementierung der IEnumSTATPROPSTG-Compound Datei

Die Implementierung der Verbund Datei der [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) -Schnittstelle wird zum Auflisten von Eigenschaften verwendet. Dies führt zu [**Status**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) Werten, die statistische Eigenschaften Daten enthalten. Die Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) verwaltet die statistischen Daten und ist einem aktuellen Verbund Datei-Speicher Objekt zugeordnet.

Der Konstruktor in der com-Implementierung von [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) erstellt eine Klasse, die den gesamten Eigenschaften Satz liest und ein statisches Array erstellt, das freigegeben werden kann, wenn **ienumstatus propstg:: Clone** aufgerufen wird.

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Aufrufen der Implementierung der Verbund Datei von [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) zum Auflisten der [**Status**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) Wert Strukturen, die Daten zu den Eigenschaften innerhalb des aktuellen Eigenschaften Satzes enthalten. Wenn Sie die Verbund Datei Implementierung der Eigenschaften Speicher Schnittstellen verwenden, müssen Sie [**IPropertyStorage:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) aufrufen, um einen Zeiger auf **ienumstatus propstg** zurückzugeben, um das Eigenschaften Speicher Objekt und die darin enthaltenen Elemente zu verwalten.

## <a name="remarks"></a>Bemerkungen

<dl> <dt>

<span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**Ienumstatus propstg:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Ruft das nächste oder mehrere [**Status-g**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) -Strukturen ab (die Zahl wird durch den *celt* -Parameter angegeben). Gibt \_ bei Erfolg S OK zurück.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**Ienumstatus propstg:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Überspringt die Anzahl der in *celt* angegebenen Elemente. Das nächste Element, das durch einen-aufzurufenden aufgerufen werden soll, wird das-Element nach den übersprungenen Elementen. Gibt s \_ OK zurück, wenn *celt* -Elemente übersprungen wurden; gibt den Wert false zurück, \_ Wenn weniger als *celt* -Elemente übersprungen wurden.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**Ienumstatus propstg:: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Legt den Cursor auf den Anfang der Enumeration fest. Wenn erfolgreich, wird S OK zurückgegeben; \_ andernfalls wird STG \_ E \_ InvalidHandle zurückgegeben.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**Ienumstatus propstg:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Verwendet den Konstruktor für [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , um eine Kopie des Arrays zu erstellen. Da die-Klasse, die das statische Array erstellt, tatsächlich das-Objekt enthält, fügt diese Funktion hauptsächlich den Verweis Zähler hinzu.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Status-g**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[**IPropertyStorage:: Aufzählung**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 