---
title: IDXCoreAdapterList::Sort
description: Sortiert ein DXCore-Adapterlistenobjekt basierend auf einem bereitgestellten Eingabearray von Sortierkriterien.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 59580fb8b76c80a264796f829d2b0a1d2e8eabb4375896fbd27fb34a7697cf90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278871"
---
# <a name="idxcoreadapterlistsort-method"></a>IDXCoreAdapterList::Sort-Methode

## <a name="description"></a>Beschreibung

Sortiert ein DXCore-Adapterlistenobjekt basierend auf einem bereitgestellten Eingabearray von Sortierkriterien, wobei Arrayelementen weiter oben im Kriterienarray eine höhere Gewichtung erteilt wird. **Sortieren** hilft Ihnen, Ihren idealen Adapter einfacher in einer Adapterliste zu finden.

## <a name="syntax"></a>Syntax

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a>Parameter

### <a name="numpreferences"></a>numPreferences

Typ: **uint32_t**

Die Anzahl der Elemente im Array, auf die der *Preferences-Parameter* zeigt.

### <a name="preferences-in"></a>Preferences [in]

Typ: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***

Ein Zeiger auf ein konstantes Array [von DXCoreAdapterPreference-Werten,](./ne-dxcore_interface-dxcoreadapterpreference.md) die Sortierkriterien darstellen.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ist, gibt **sie** S_OK. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [zurückgegeben.](../../com/com-error-codes-10.md)

|Rückgabewert|Beschreibung|
|-|-|
|E_INVALIDARG|Das *argument numPreferences* ist 0 (null), oder *das Preferences-Argument* ist `nullptr` .|

## <a name="remarks"></a>Hinweise

In Fällen, in denen ein bereitgestellter [DXCoreAdapterPreference-Wert](./ne-dxcore_interface-dxcoreadapterpreference.md) vom Betriebssystem nicht erkannt wird, wird er ignoriert und führt nicht dazu, dass die API fehlschlägt. Bekannte **DXCoreAdapterPreference-Werte** werden in diesem Fall weiterhin berücksichtigt. Um zu bestimmen, ob ein Sortiertyp von der API verstanden wird, rufen Sie [IDXCoreAdapterList::IsAdapterPreferenceSupported auf.](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md)

**DXCoreAdapterPreference-Werte,** die zuvor im angegebenen *Preferences-Array* auftreten, werden mit höherer Priorität behandelt. 

Weitere Informationen dazu, welche Logik für die einzelnen Typen angewendet wird, finden Sie in der **DXCoreAdapterPreference-Enumerationsdokumentation.** Die interne Logik für einen Typ kann sich während der Entwicklung des Betriebssystems entwickeln.

Nach der Rückgabe von **Sort** wurden elemente in der DXCore-Adapterliste von den am wenigsten bevorzugten elementen sortiert. Daher ruft der [Aufruf von IDXCoreAdapterList::GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) mit Index 0 den Adapter ab, der den angeforderten Sortierpräferenztypen am besten entspricht. Index 1 ist die nächste beste Übereinstimmung, und so weiter.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), Verwenden von DXCore zum [Auflisten von Adaptern](../dxcore-enum-adapters.md)