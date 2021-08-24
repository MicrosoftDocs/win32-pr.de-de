---
title: IWMDRMLicense GetInclusionList-Methode (Wmdrmsdk.h)
description: Die GetInclusionList-Methode ruft die gesamte Aufnahmeliste für die aktuelle Lizenz oder Lizenzkette ab.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- GetInclusionList-Methode windows Media Format
- GetInclusionList-Methode windows Media Format, IWMDRMLicense-Schnittstelle
- IWMDRMLicense-Schnittstelle windows Media Format , GetInclusionList-Methode
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
ms.openlocfilehash: 6389ac30d5bffeb6ad354ec6c7e83f2834921fe8fb83c1abe2bca2d0c2f43bfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705240"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a>IWMDRMLicense::GetInclusionList-Methode

Die **GetInclusionList-Methode** ruft die gesamte Aufnahmeliste für die aktuelle Lizenz oder Lizenzkette ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppGuids* \[ out\]
</dt> <dd>

Empfängt ein Array von GUIDs, die die enthaltenen Technologien identifizieren.

</dd> <dt>

*pcGuids* \[ out\]
</dt> <dd>

Empfängt die Anzahl der Elemente im *ppGuids-Array.* Das Array wird mithilfe von **CoTaskMemAlloc zugeordnet.** Wenn Sie mit der Liste fertig sind, geben Sie den Arbeitsspeicher frei, indem **Sie CoTaskMemFree aufrufen.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Lizenzaussteller kann andere Schutzsysteme angeben, in die der verschlüsselte Inhalt konvertiert werden kann. Die Liste der von dieser Methode abgerufenen GUIDs identifiziert die zulässigen Schutzsysteme. Wenn Sie einen Lizenzvertrag mit Microsoft zum Erhalten der Stubbibliothek unterzeichnet haben, erhalten Sie eine Liste der derzeit unterstützten Schutzsysteme und die GUIDs, mit denen sie identifiziert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Explizite Autorisierungs- und Einschlusslisten**](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





