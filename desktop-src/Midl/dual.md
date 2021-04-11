---
title: dual-Attribut
description: Das Dual-Attribut identifiziert eine Schnittstelle, die Eigenschaften und Methoden über IDispatch und direkt über den VTBL verfügbar macht.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- Dual Attribute-Mittel l
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39a9e44de464f58fd1ffc0606551b9a0203ae9e9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948722"
---
# <a name="dual-attribute"></a>dual-Attribut

Das **Dual** -Attribut identifiziert eine Schnittstelle, die Eigenschaften und Methoden über [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) und direkt über den VTBL verfügbar macht.

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*UUID-Nummer* 
</dt> <dd>

Gibt eine universell eindeutige Identifikationsnummer für die Schnittstelle an.

</dd> <dt>

*optional-Attribut-List* 
</dt> <dd>

Gibt eine Liste von 0 (null) oder mehr zusätzlichen Mittelwert Attributen an.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Der Name der Schnittstelle, auf die das **Dual** -Attribut angewendet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Schnittstellen, die durch das **Dual** -Attribut identifiziert werden, müssen mit Automation kompatibel sein und von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)abgeleitet werden. Dieses Attribut ist für dispinterfaces nicht zulässig.

Das **Dual** -Attribut erstellt eine Schnittstelle, die sowohl eine [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle als auch eine Component Object Model (com)-Schnittstelle ist. Die ersten sieben Einträge der VTBL für eine duale Schnittstelle sind die sieben Member von **IDispatch**, und die restlichen Einträge sind für den direkten Zugriff auf Member der Dual-Schnittstelle. Alle Parameter und Rückgabe Typen, die für Member einer Dual-Schnittstelle angegeben sind, müssen Automatisierungs kompatible Typen sein.

Alle Member einer Dual-Schnittstelle müssen ein HRESULT als Rückgabewert der Funktion übergeben. Member, z. b. eigenschaftenaccessorfunktionen, die andere Werte zurückgeben müssen, sollten den letzten Parameter als " [**out**](out-idl.md)", " [**retval**](retval.md)" angeben, der einen Ausgabeparameter angibt, der den Wert der Funktion zurückgibt. Außerdem sollten Member, die mehrere Gebiets Schemas unterstützen müssen, einen [**LCID**](lcid.md) -Parameter übergeben.

Eine duale Schnittstelle ermöglicht sowohl die Geschwindigkeit der direkten VTBL-Bindung als auch die Flexibilität der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Bindung. Aus diesem Grund werden zwei Schnittstellen empfohlen, wann immer dies möglich ist.

> [!Note]  
> Wenn Ihre Anwendung auf Objektdaten zugreift, indem Sie *den Zeiger in den Schnittstellen* aufzurufen umwandeln, sollten Sie die VTBL-Zeiger im Objekt anhand ihrer eigenen VTBL-Zeiger überprüfen, um sicherzustellen, dass Sie mit dem entsprechenden Proxy verbunden sind.

 

Das Angeben von **Dual** für eine Schnittstelle impliziert, dass die Schnittstelle mit Automation kompatibel ist, sodass sowohl das TYPEFLAG \_ fdual-als auch das TYPEFLAG \_ foleautomation-Flag festgelegt werden.

### <a name="flags"></a>Flags

TYPEFLAG ( \_ odual), TYPEFLAG \_ foleautomation

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 