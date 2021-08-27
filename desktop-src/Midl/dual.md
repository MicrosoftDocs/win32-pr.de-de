---
title: dual-Attribut
description: Das duale Attribut identifiziert eine Schnittstelle, die Eigenschaften und Methoden über IDispatch und direkt über die VTBL verfügbar macht.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- MIDL mit dualen Attributen
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e1e9cd15c1b219d07518c9630880a5010226c96c63d57539ffb66fab3a6c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643094"
---
# <a name="dual-attribute"></a>dual-Attribut

Das **duale** Attribut identifiziert eine Schnittstelle, die Eigenschaften und Methoden über [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) und direkt über die VTBL verfügbar macht.

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

*uuid-number* 
</dt> <dd>

Gibt eine universell eindeutige ID für die Schnittstelle an.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Gibt eine Liste mit null oder mehr zusätzlichen MIDL-Attributen an.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Der Name der Schnittstelle, auf die das **duale** Attribut angewendet wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Schnittstellen, die durch das **duale** Attribut identifiziert werden, müssen mit Automation kompatibel sein und von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)abgeleitet werden. Dieses Attribut ist für dispinterfaces nicht zulässig.

Das **duale** Attribut erstellt eine Schnittstelle, die sowohl eine [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) als auch eine com-Schnittstelle (Component Object Model) ist. Die ersten sieben Einträge der VTBL für eine duale Schnittstelle sind die sieben Member von **IDispatch,** und die verbleibenden Einträge dienen dem direkten Zugriff auf Member der dualen Schnittstelle. Alle Parameter und Rückgabetypen, die für Member einer dualen Schnittstelle angegeben sind, müssen Automation-kompatible Typen sein.

Alle Member einer dualen Schnittstelle müssen ein HRESULT als Rückgabewert der Funktion übergeben. Member, z. B. Eigenschaftenaccessorfunktionen, die andere Werte zurückgeben müssen, sollten den letzten Parameter als [**out**](out-idl.md)angeben, [**erneut**](retval.md)ausführen und einen Ausgabeparameter angeben, der den Wert der Funktion zurückgibt. Darüber hinaus sollten Member, die mehrere Gebietsschemas unterstützen müssen, einen [**lcid-Parameter**](lcid.md) übergeben.

Eine duale Schnittstelle bietet sowohl die Geschwindigkeit der direkten VTBL-Bindung als auch die Flexibilität der [**IDispatch-Bindung.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Aus diesem Grund werden nach Möglichkeit duale Schnittstellen empfohlen.

> [!Note]  
> Wenn Ihre Anwendung auf Objektdaten zugreift, indem sie *diesen* Zeiger innerhalb des Schnittstellenaufrufs umleitet, sollten Sie die VTBL-Zeiger im -Objekt anhand Ihrer eigenen VTBL-Zeiger überprüfen, um sicherzustellen, dass Sie mit dem entsprechenden Proxy verbunden sind.

 

Die Angabe von **dual** für eine Schnittstelle impliziert, dass die Schnittstelle mit Automation kompatibel ist. Daher werden sowohl die TYPEFLAG-FDUAL- als auch \_ die TYPEFLAG \_ FOLEAUTOMATION-Flags festgelegt.

### <a name="flags"></a>Flags

TYPEFLAG \_ FDUAL, TYPEFLAG \_ FOLEAUTOMATION

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

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Retval**](retval.md)
</dt> </dl>

 

 