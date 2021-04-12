---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Generiert eine Liste von Adapter Objekten, die den aktuellen Adapter Zustand des Systems darstellen, und erfüllt die angegebenen Kriterien.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473748"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a>Idxcoreadapterfactory:: kreateadapterlist-Methode

Generiert eine Liste von Adapter Objekten, die den aktuellen Adapter Zustand des Systems darstellen, und erfüllt die angegebenen Kriterien. Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).

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

### <a name="numattributes"></a>numattribute

Typ: **uint32_t**

Die Anzahl der Elemente im Array, auf die vom *filterattributerargument* verwiesen wird.

### <a name="filterattributes-in"></a>Filterattribute [in]

Typ: Konstante **GUID \***

Ein Zeiger auf ein Array von adapterattributguids. Eine Liste der Attribut-GUIDs finden Sie unter [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md). Mindestens eine GUID muss angegeben werden. Wenn mehr als eine GUID im Array bereitgestellt wird, werden nur Adapter, die *alle* angeforderten Attribute erfüllen, in der zurückgegebenen Liste enthalten sein.

### <a name="riid"></a>riid

Typ: **refID**

Ein Verweis auf die Globally Unique Identifier (GUID) der Schnittstelle, die in *ppvadapterlist* zurückgegeben werden soll. Dies wird als Schnittstellen Bezeichner (IID) von [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md)erwartet.

### <a name="ppvadapterlist-out"></a>ppvadapterlist [out]

Typ: **void \* \***

Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid* -Parameter angegebenen IID. Bei erfolgreicher Rückgabe enthält *\* ppvadapterlist* (die Dereferenzierte Adresse) einen Zeiger auf die erstellte Adapter Liste.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|E_INVALIDARG|`nullptr` wurde für *Filter Attribute* bereitgestellt, oder 0 wurde für *numattribute* bereitgestellt.|
|E_NOINTERFACE|Für *riid* wurde ein ungültiger Wert angegeben.|
|E_POINTER|`nullptr` wurde für *ppvadapterlist* bereitgestellt.|

## <a name="remarks"></a>Bemerkungen

Auch wenn keine Adapter gefunden werden, erstellt " **kreateadapterlist** " ein gültiges [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md) -Objekt und gibt **S_OK** zurück, solange die Argumente gültig sind. Nach der Generierung werden die Adapter in dieser bestimmten Liste nicht geändert. Die Liste wird jedoch als veraltet eingestuft, wenn einer der Adapter später ungültig wird oder wenn ein neuer Adapter eintrifft, der die angegebenen Filterkriterien erfüllt. Die von " **kreateadapterlist** " zurückgegebene Liste ist nicht auf bestimmte Weise geordnet, aber die Reihenfolge einer Liste ist über mehrere Aufrufe hinweg konsistent und auch über Betriebssystem Neustarts hinweg. Die Reihenfolge kann sich bei Änderungen der Systemkonfiguration ändern, einschließlich des Hinzufügens oder Entfernens eines Adapters oder eines Treiber Updates für einen vorhandenen Adapter. Sie können sich für diese Änderungen mit [idxcoreadapterfactory:: registereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) mithilfe des Benachrichtigungs Typs **dxcorenotificationtype. adapterliststale** registrieren.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)