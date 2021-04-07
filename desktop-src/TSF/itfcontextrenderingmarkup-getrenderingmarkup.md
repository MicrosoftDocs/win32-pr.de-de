---
title: ITF contextrenderingmarkup GetRenderingMarkup-Methode
description: Die ITF contextrenderingmarkup GetRenderingMarkup-Methode ruft einen Enumerator der rendermarkups für den angegebenen Bereich ab.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- GetRenderingMarkup-Methode-Text Dienst-Framework
- GetRenderingMarkup Method Text Services Framework, ITF contextrenderingmarkup-Schnittstelle
- ITF contextrenderingmarkup Interface Text Services Framework, GetRenderingMarkup-Methode
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f3ccfb97af6a6657c33982359640a2a924cad2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728553"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a>ITF contextrenderingmarkup:: GetRenderingMarkup-Methode

Die **ITF contextrenderingmarkup:: GetRenderingMarkup** -Methode ruft einen Enumerator der rendermarkups für den angegebenen Bereich ab.

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

*EC* \[ in\]
</dt> <dd>

\[in \] einem schreibgeschützten Bearbeitungs Cookie, um auf den Kontext zuzugreifen.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

\[in\]



| Wert                                                                                                                                                                                         | Bedeutung                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <dt>**TF \_ GRM \_ include- \_ Eigenschaft**</dt> </dl> | Wenn dieses Bit 1 ist, enthält der Enumerator die GUID- \_ Eigenschaft des prop- \_ Attributs.<br/> |



 

</dd> <dt>

*prangecover* \[ in\]
</dt> <dd>

\[in \] einem Zeiger auf eine [itfrange](/windows/desktop/api/Msctf/nn-msctf-itfrange) -Schnittstelle des Bereichs zum Aufzählen der rendermarkups.

</dd> <dt>

*ppum* \[ vorgenommen\]
</dt> <dd>

\[\]ein Zeiger zum Abrufen des [ienumtfrenderingmarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) -Schnittstellen Zeigers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                | BESCHREIBUNG                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Diese Methode befindet sich derzeit nicht in den öffentlichen Header Dateien. Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.

 

 

