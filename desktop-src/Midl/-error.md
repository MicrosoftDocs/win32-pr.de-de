---
title: /Error-Schalter
description: Der Schalter/Error bestimmt die Typen der Fehlerüberprüfung, die von den generierten stubvorschauen zur Laufzeit ausgeführt werden.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- /Error-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84a56c1ae3d57ab1931ec175aa8dc9010ea6b8a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389259"
---
# <a name="error-switch"></a>/Error-Schalter

Der Schalter **/Error** bestimmt die Typen der Fehlerüberprüfung, die von den generierten stubvorschauen zur Laufzeit ausgeführt werden.

> [!Note]  
> Diese Funktion ist veraltet und wird nicht mehr unterstützt. Die Verwendung des [**/robust**](-robust.md) -Schalters wird empfohlen.

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span id="allocation"></span><span id="ALLOCATION"></span>Zuordnung * * * *


</dt> <dd>

Überprüft, ob der Wert für die [**mittlere \_ Benutzer \_ Zuteilung**](midl-user-allocate-1.md) einen **null** -Wert zurückgibt, der auf einen Fehler wegen nicht genügend Arbeitsspeichers hinweist.

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span id="stub_data"></span><span id="STUB_DATA"></span>Stub- \_ Daten * * * *


</dt> <dd>

Generiert einen Stub, der das Marshalling von Ausnahmen auf der Serverseite abfängt und Sie an den Client zurückgibt.

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span id="ref"></span><span id="REF"></span>Ref * * * *


</dt> <dd>

Generiert Code, der zur Laufzeit eine Überprüfung ausführt, um sicherzustellen, dass keine **null** -Verweis Zeiger an die clientstubwerte übermittelt werden, und löst eine RPC-X-NULL-Verweis \_ Zeiger Ausnahme aus, \_ \_ \_ Wenn eine gefunden wird.

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>Begrenzungen \_ Überprüfung * * * *


</dt> <dd>

Überprüft die Größe des konformen und variierenden Arrays anhand der Angabe der Übertragungs Länge.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>keine * * * *


</dt> <dd>

Führt keine Fehlerüberprüfung aus.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>Alle * * * *


</dt> <dd>

Führt alle Fehlerprüfungen aus. Dies ist eine standardmäßige Compileroption, die mit der mittleren Version 5,0 wirksam ist.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Schalter **/Error** wählt die Anzahl der Fehlerüberprüfungen aus, die von den generierten Stub-Dateien durchgeführt werden. Gültig mit der mittleren Version 5,0, ist die Standardeinstellung " **/Error all**".

Die aktivierten Enumerationsfehler (standardmäßig in allen Versionen von "Mittel l") sind abkürzen, die bei der Umstellung zwischen **langen** Enumerationstypen (32-Bit-Ganzzahlen) und **kurzen** Enumerationstypen (der Netzwerkdaten [**Darstellung der**](enum.md)Enumeration) und der Anzahl der Bezeichner in einer Enumeration, die 32.767 überschreitet, verursacht werden.

Die Speicherzugriffs Fehlerüberprüfung (auch standardmäßig in allen Versionen von "Mittel l") ist für Zeiger vorgesehen, die das Ende des Puffers im Marshalling von Code überschreiten, sowie für konforme Arrays, deren Größe kleiner als 0 (null) ist. Verwenden **\_ Sie das Kontroll Flag/Error Bounds** , um andere ungültige Array Begrenzungen zu überprüfen.

Wenn Sie die **/Error-Zuordnung** angeben, enthalten die stubsteine Code, der eine Ausnahme auslöst, wenn die [**mittlere \_ Benutzer \_ Zuordnung**](midl-user-allocate-1.md) 0 zurückgibt.

Mit der **/Error Stub \_ Data** -Option wird verhindert, dass Client Daten während des Unmarshalling auf den Server abstürzen und somit eine stabilere Methode zur Behandlung des nicht Marshallingvorgangs bereitstellen.

Mit Windows-2000 werden die meisten dieser Überprüfungen von der zugrunde liegenden Lauf Zeit-NDR-Mars Hall-Engine ausgeführt. Dies bedeutet Folgendes: Wenn Sie einen der voll interpretierten Modi ([**/Oi**](-oi.md), **/OIF**) der Stub-Generierung verwenden, hat die Auswahl verschiedener Optionen für die Fehlerüberprüfung keine markierte Auswirkung auf die Leistung.

## <a name="examples"></a>Beispiele

**Mittel l/Error Zuordnungs Dateiname. idl**

**Mittel l/Error keine Datei Name. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




