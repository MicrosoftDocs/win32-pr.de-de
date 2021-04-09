---
title: IDXCoreAdapterList::Sort
description: Sortiert ein DXCore-Adapter Listen Objekt auf Grundlage eines angegebenen Eingabe Arrays von Sortierkriterien.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102195"
---
# <a name="idxcoreadapterlistsort-method"></a>Idxcoreadapterlist:: Sort-Methode

## <a name="description"></a>BESCHREIBUNG

Sortiert ein DXCore-Adapter Listen Objekt auf Grundlage eines angegebenen Eingabe Arrays von Sortierkriterien, wobei Array Elemente an früherer Stelle im Array von Kriterien eine höhere Gewichtung erhalten. Mit **Sort** können Sie den idealen Adapter leichter in einer Adapter Liste finden.

## <a name="syntax"></a>Syntax

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a>Parameter

### <a name="numpreferences"></a>numpreferences

Typ: **uint32_t**

Die Anzahl der Elemente im Array, auf die durch den *Preferences* -Parameter verwiesen wird.

### <a name="preferences-in"></a>Einstellungen [in]

Typ: Konstante **[dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***

Ein Zeiger auf ein konstantes Array von [dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md) -Werten, das Sortierkriterien darstellt.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|E_INVALIDARG|Das *numpreferences* -Argument ist 0 (null), oder das *Preferences* -Argument ist `nullptr` .|

## <a name="remarks"></a>Bemerkungen

In Fällen, in denen ein bereitgestellter [dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md) -Wert vom Betriebssystem (OS) nicht erkannt wird, wird er ignoriert und führt nicht zu einem Fehler bei der API. Bekannte **dxcoreadapterpreference** -Werte werden in diesem Fall weiterhin berücksichtigt. Um zu ermitteln, ob ein Sortierungstyp von der API verstanden wird, nennen Sie [idxcoreadapterlist:: isadapterpreferencesupportiert](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).

**Dxcoreadapterpreference** -Werte, die zuvor im angegebenen *Einstellungs* Array auftreten, werden mit höherer Priorität behandelt. 

Ausführliche Informationen dazu, welche Logik für die einzelnen Typen angewendet wird, finden Sie in der Dokumentation zur **dxcoreadapterpreference** -Enumeration. Die interne Logik für einen Typ kann sich entwickeln, wenn das Betriebssystem entwickelt wird.

Wenn " **Sort** " zurückgegeben wird, wurden Elemente in der DXCore-Adapter Liste nach den am wenigsten bevorzugten Elementen sortiert. Wenn Sie daher [idxcoreadapterlist:: GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) mit dem Index 0 aufrufen, wird der Adapter abgerufen, der den angeforderten Sortier Einstellungs Typen am besten entspricht. Index 1 ist die nächste am besten geeignete Entsprechung usw.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)