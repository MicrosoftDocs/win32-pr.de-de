---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Generiert eine Liste von Adapterobjekten, die den aktuellen Adapterstatus des Systems darstellen und die angegebenen Kriterien erfüllen.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0d00cba3236bf63a1691473098b1f94438b790a93a75215e36690745ee7977fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842520"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a>IDXCoreAdapterFactory::CreateAdapterList-Methode

Generiert eine Liste von Adapterobjekten, die den aktuellen Adapterstatus des Systems darstellen und die angegebenen Kriterien erfüllen. Programmierleitfäden und Codebeispiele finden Sie unter [Verwenden von DXCore zum Aufzählen von Adaptern.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a>Parameter

### <a name="numattributes"></a>numAttributes

Typ: **uint32_t**

Die Anzahl der Elemente im Array, auf die das *filterAttributes-Argument* zeigt.

### <a name="filterattributes-in"></a>filterAttributes [in]

Typ: **const \* GUID**

Ein Zeiger auf ein Array von Adapterattribut-GUIDs. Eine Liste der Attribut-GUIDs finden Sie unter [DXCore-Adapterattribut-GUIDs.](../dxcore-adapter-attribute-guids.md) Mindestens eine GUID muss bereitgestellt werden. Falls mehr als eine GUID im Array bereitgestellt wird, werden nur Adapter, die *alle* angeforderten Attribute erfüllen, in die zurückgegebene Liste aufgenommen.

### <a name="riid"></a>riid

Typ: **REFIID**

Ein Verweis auf die GUID (Globally Unique Identifier) der Schnittstelle, die in *ppvAdapterList* zurückgegeben werden soll. Es wird erwartet, dass dies der Schnittstellenbezeichner (IID) von [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)ist.

### <a name="ppvadapterlist-out"></a>ppvAdapterList [out]

Typ: **\* \* void**

Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid-Parameter* angegebenen IID. Nach erfolgreicher Rückgabe enthält *\* ppvAdapterList* (die dereferenzierte Adresse) einen Zeiger auf die erstellte Adapterliste.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|E_INVALIDARG|`nullptr` wurde für *filterAttributes* bereitgestellt, oder 0 wurde für *numAttributes* bereitgestellt.|
|E_NOINTERFACE|Für *riid* wurde ein ungültiger Wert bereitgestellt.|
|E_POINTER|`nullptr` wurde für *ppvAdapterList* bereitgestellt.|

## <a name="remarks"></a>Hinweise

Auch wenn keine Adapter gefunden werden, erstellt **CreateAdapterList** ein gültiges [IDXCoreAdapterList-Objekt](./nn-dxcore_interface-idxcoreadapterlist.md) und gibt **S_OK** zurück. Nach der Generierung ändern sich die Adapter in dieser spezifischen Liste nicht mehr. Die Liste gilt jedoch als veraltet, wenn einer der Adapter später ungültig wird oder ein neuer Adapter eintrifft, der die angegebenen Filterkriterien erfüllt. Die von **CreateAdapterList** zurückgegebene Liste ist in keiner bestimmten Weise sortiert, aber die Reihenfolge einer Liste ist über mehrere Aufrufe hinweg und sogar bei Betriebssystemneustarts konsistent. Die Reihenfolge kann sich bei Änderungen der Systemkonfiguration ändern, einschließlich des Hinzufügens oder Entfernens eines Adapters oder eines Treiberupdates für einen vorhandenen Adapter. Sie können sich für diese Änderungen mit [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) registrieren, indem Sie den Benachrichtigungstyp **DXCoreNotificationType.AdapterList State** verwenden.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapterFactory,](./nn-dxcore_interface-idxcoreadapterfactory.md) [DXCore-Referenz,](../dxcore-reference.md) [DXCore-Adapterattribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)