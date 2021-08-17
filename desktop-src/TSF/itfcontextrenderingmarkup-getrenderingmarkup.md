---
title: ITfContextRenderingMarkup GetRenderingMarkup-Methode
description: Die ITfContextRenderingMarkup GetRenderingMarkup-Methode ruft einen Enumerator der Renderingmarkups für den angegebenen Bereich ab.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- GetRenderingMarkup-Textdienstframework
- GetRenderingMarkup-Methode Textdienstframework , ITfContextRenderingMarkup-Schnittstelle
- ITfContextRenderingMarkup-Schnittstelle Textdienstframework , GetRenderingMarkup-Methode
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a94c8a7cce8673560cf01091b819def343213bfde578df6ce1e8850e2721723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476954"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a>ITfContextRenderingMarkup::GetRenderingMarkup-Methode

Die **ITfContextRenderingMarkup::GetRenderingMarkup-Methode** ruft einen Enumerator der Renderingmarkups für den angegebenen Bereich ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ec* \[ In\]
</dt> <dd>

\[in \] Ein schreibgeschütztes Bearbeitungscookie für den Zugriff auf den Kontext.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

\[in\]



| Wert                                                                                                                                                                                         | Bedeutung                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <dt>**TF \_ GRM \_ \_ INCLUDE-EIGENSCHAFT**</dt> </dl> | Wenn dieses Bit 1 ist, enthält der Enumerator die EIGENSCHAFT GUID \_ PROP \_ ATTRIBUTE.<br/> |



 

</dd> <dt>

*pRangeCover* \[ In\]
</dt> <dd>

\[in \] Ein Zeiger auf eine [ITfRange-Schnittstelle](/windows/desktop/api/Msctf/nn-msctf-itfrange) des Bereichs zum Aufzählen der Renderingmarkups.

</dd> <dt>

*ppEnum* \[ out\]
</dt> <dd>

\[out \] Ein Zeiger zum Abrufen des [IEnumTfRenderingMarkup-Schnittstellenzeigers.](/windows/desktop/TSF/ienumtfrenderingmarkup)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                | BESCHREIBUNG                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Diese Methode befindet sich derzeit nicht in den öffentlichen Headerdateien. Um diese API zu verwenden, müssen Sie den Prototyp [midl-kompilieren.](prototypes.md)

 

 

