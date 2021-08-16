---
description: Die ISampleGrabberCB-Schnittstelle stellt Rückrufmethoden für die ISampleGrabber::SetCallback-Methode bereit. Wenn Ihre Anwendung diese Methode aufruft, muss sie diese Schnittstelle implementieren. Weitere Informationen finden Sie unter ISampleGrabber.
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: ISampleGrabberCB-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 822eef97ebd2ff169631f0e4d83cdfe3417388389e112851f5e77dcd7216acfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817502"
---
# <a name="isamplegrabbercb-interface"></a>ISampleGrabberCB-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `ISampleGrabberCB` -Schnittstelle stellt Rückrufmethoden für die [**ISampleGrabber::SetCallback-Methode**](isamplegrabber-setcallback.md) bereit. Wenn Ihre Anwendung diese Methode aufruft, muss sie diese Schnittstelle implementieren. Weitere Informationen finden Sie unter [**ISampleGrabber**](isamplegrabber.md).

## <a name="members"></a>Member

Die **ISampleGrabberCB-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISampleGrabberCB** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISampleGrabberCB-Schnittstelle** verfügt über diese Methoden.



| Methode                                        | Beschreibung                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**BufferCB**](isamplegrabbercb-buffercb.md) | Rückrufmethode, die einen Zeiger auf den Beispielpuffer empfängt.<br/> |
| [**SampleCB**](isamplegrabbercb-samplecb.md) | Rückrufmethode, die einen Zeiger auf das Medienbeispiel empfängt.<br/>  |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
