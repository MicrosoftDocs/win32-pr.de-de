---
description: Ruft das nächste untergeordnete Datenobjekt, das Daten Verweis Objekt oder das binäre Objekt in der DirectX-Datei ab. Veraltet.
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'Idirectxfiledata:: getnextobject-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371935"
---
# <a name="idirectxfiledatagetnextobject-method"></a>Idirectxfiledata:: getnextobject-Methode

Ruft das nächste untergeordnete Datenobjekt, das Daten Verweis Objekt oder das binäre Objekt in der DirectX-Datei ab. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppchildobj* \[ Out, retval\]
</dt> <dd>

Typ: **[ **lpdirectxfileobject**](idirectxfileobject.md)\***

Adresse eines Zeigers auf eine [**idirectxfileobject**](idirectxfileobject.md) -Schnittstelle, die die Datei Objektschnittstelle des zurückgegebenen untergeordneten Objekts darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badvalue, dxfileerr \_ nomoreobjects.

## <a name="remarks"></a>Bemerkungen

Um den Typ des abgerufenen Objekts zu ermitteln, verwenden Sie QueryInterface, um das abgerufene Objekt zur Unterstützung der Schnittstellen [**idirectxfiledata**](idirectxfiledata.md), [**idirectxfiledatareferenoder**](idirectxfiledatareference.md) [**idirectxfilebinary**](idirectxfilebinary.md) abzufragen. Die unterstützte Schnittstelle zeigt den Objekttyp an (Daten, Daten Verweis oder binär).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idirectxfilebinary**](idirectxfilebinary.md)
</dt> <dt>

[**Idirectxfiledata**](idirectxfiledata.md)
</dt> <dt>

[**Idirectxfiledatareferenzierung**](idirectxfiledatareference.md)
</dt> </dl>

 

 




