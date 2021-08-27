---
title: /error-Schalter
description: Der Schalter /error bestimmt die Typen der Fehlerüberprüfung, die die generierten Stubs zur Laufzeit ausführen.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- /error switch MIDL
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7af27de3d83171c8f1f89d0b860bf0b38ddfb6639a12bf40f90a58f06a273cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105630"
---
# <a name="error-switch"></a>/error-Schalter

Der Schalter **/error** bestimmt die Typen der Fehlerüberprüfung, die die generierten Stubs zur Laufzeit ausführen.

> [!Note]  
> Dieses Feature ist veraltet und wird nicht mehr unterstützt. Die Verwendung des Schalters [**/robust**](-robust.md) wird empfohlen.

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span id="allocation"></span><span id="ALLOCATION"></span>allocation(


</dt> <dd>

Überprüft, ob [**midl \_ user \_ allocate**](midl-user-allocate-1.md) einen **NULL-Wert** zurückgibt, der auf einen Fehler mit nicht genügend Arbeitsspeicher hinweist.

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span id="stub_data"></span><span id="STUB_DATA"></span>stub \_ data(


</dt> <dd>

Generiert einen Stub, der Ausnahmen auf serverseitiger Seite abfängt und an den Client zurücksendet.

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span id="ref"></span><span id="REF"></span>ref!


</dt> <dd>

Generiert Code, der zur Laufzeit eine Überprüfung ausführt, um sicherzustellen, dass keine **NULL-Verweiszeiger** an die Clientstubs übergeben werden, und löst ggf. eine RPC \_ X NULL REF \_ \_ \_ POINTER-Ausnahme aus.

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>bounds \_ check(


</dt> <dd>

Überprüft die Größe konformer und variierender Arrays anhand der Spezifikation der Übertragungslänge.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>none(


</dt> <dd>

Führt keine Fehlerüberprüfung aus.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>all(


</dt> <dd>

Führt alle Fehlerüberprüfungen aus. Ab MIDL-Version 5.0 ist dies ein Standardcompilerschalter.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Der Schalter **/error** wählt die Anzahl der Fehlerüberprüfungen aus, die die generierten Stubdateien ausführen. Ab MIDL Version 5.0 ist die Standardeinstellung **/error all**.

Bei den überprüften Enumerationsfehlern (standardmäßig in allen Versionen von MIDL) handelt es sich um Kürzungsfehler, die beim Konvertieren zwischen **langen Enumerationstypen** (32-Bit-Ganzzahlen) und kurzen Enumerationstypen (die Darstellung von **Enumerationen** im Netzwerkdaten) und der Anzahl von Bezeichnern in einer Enumeration, die 32.767 überschreiten, verursacht werden. [](enum.md)

Die Speicherzugriffsfehlerüberprüfung (auch standardmäßig in allen Versionen von MIDL) gilt für Zeiger, die das Ende des Puffers im Marshallingcode überschreiten, und für konforme Arrays, deren Größe kleiner als 0 (null) ist. Verwenden Sie das **\_ Häkchen /error bounds,** um nach anderen ungültigen Arraygrenzen zu suchen.

Wenn Sie **/error allocation** angeben, enthalten die Stubs Code, der eine Ausnahme auslöst, wenn [**midl user \_ \_ allocate**](midl-user-allocate-1.md) 0 zurückgibt.

Die **\_ Stubdatenoption /error** verhindert, dass Clientdaten während des Unmarshalings auf den Server abstürzten, was effektiv eine stabilere Methode zur Behandlung des Unmarshalingvorgangs bietet.

Ab Windows 2000 führt die zugrunde liegende NDR-Marshalling-Engine zur Laufzeit die meisten dieser Überprüfungen durch. Dies bedeutet Folgendes: Wenn Sie einen der vollständig interpretierten Modi [**(/Oi**](-oi.md), **/Oif**) der Stubgenerierung verwenden, hat die Auswahl verschiedener Optionen für die Fehlerüberprüfung keine markierten Auswirkungen auf die Leistung.

## <a name="examples"></a>Beispiele

**midl /error allocation filename.idl**

**midl /error none filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




