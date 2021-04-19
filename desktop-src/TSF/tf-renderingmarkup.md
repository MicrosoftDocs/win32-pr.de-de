---
title: TF_RENDERINGMARKUP Struktur
description: Die TF \_ renderingmarkup-Struktur Struktur enthält einen Bereich und die Informationen zum Anzeige Attribut.
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- TF_RENDERINGMARKUP Struktur-Text Dienst-Framework
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342314"
---
# <a name="tf_renderingmarkup-structure"></a>TF \_ renderingmarkup-Struktur

Die [**tf \_ renderingmarkup**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) -Struktur Struktur enthält einen Bereich und die Informationen zum Anzeige Attribut.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a>Member

<dl> <dt>

**Prange**
</dt> <dd>

Ein Zeiger auf eine [itfrange](/windows/desktop/api/Msctf/nn-msctf-itfrange) -Schnittstelle.

</dd> <dt>

**tfdisplayattr**
</dt> <dd>

Attributinformationen anzeigen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur befindet sich derzeit nicht in den öffentlichen Header Dateien. Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.

 

 




