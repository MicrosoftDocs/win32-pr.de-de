---
title: Iwmdrmlicense getinclusionlist-Methode (wmdrmsdk. h)
description: Die getinclusionlist-Methode ruft die gesamte Inklusions Liste für die aktuelle Lizenz oder Lizenz Kette ab.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Getinclusionlist-Methode, Windows Media-Format
- Getinclusionlist-Methode, Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, getinclusionlist-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0d2837a4bb84c07214cce3e4fbc3d4d96b9583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367427"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a>Iwmdrmlicense:: getinclusionlist-Methode

Die **getinclusionlist** -Methode ruft die gesamte Inklusions Liste für die aktuelle Lizenz oder Lizenz Kette ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppguids* \[ vorgenommen\]
</dt> <dd>

Empfängt ein Array von GUIDs, das die enthaltenen Technologien identifiziert.

</dd> <dt>

*pcguids* \[ vorgenommen\]
</dt> <dd>

Empfängt die Anzahl der Elemente im *ppguids* -Array. Das Array wird mithilfe von **cotaskmemzuzuordnungs** zugeordnet. Wenn Sie mit der Liste fertig sind, geben Sie den Arbeitsspeicher frei, indem Sie **CoTaskMemFree** aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Mit dem Lizenz Aussteller können andere Schutzsysteme angegeben werden, in die der verschlüsselte Inhalt konvertiert werden kann. Die Liste der von dieser Methode abgerufenen GUIDs identifiziert die zulässigen Schutzsysteme. Wenn Sie in einen Lizenzvertrag von Microsoft eingeben, um die stubbibliothek zu erhalten, erhalten Sie eine Liste der derzeit unterstützten Schutzsysteme und die GUIDs, die zur Identifizierung verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Explizite Autorisierungs-und Inklusions Listen**](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[**Iwmdrmlicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





