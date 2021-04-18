---
description: 'Die isamplegrabbercb-Schnittstelle stellt Rückruf Methoden für die isamplegrabber:: SetCallback-Methode bereit. Wenn die Anwendung diese Methode aufruft, muss Sie diese Schnittstelle implementieren. Weitere Informationen finden Sie unter isamplegrabber.'
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Isamplegrabbercb-Schnittstelle (qedit. h)
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
ms.openlocfilehash: 5c39d11e6560bc5e50a4c8a9b42a1cbb095b4b71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358314"
---
# <a name="isamplegrabbercb-interface"></a>Isamplegrabbercb-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `ISampleGrabberCB` Schnittstelle stellt Rückruf Methoden für die [**isamplegrabber:: SetCallback**](isamplegrabber-setcallback.md) -Methode bereit. Wenn die Anwendung diese Methode aufruft, muss Sie diese Schnittstelle implementieren. Weitere Informationen finden Sie unter [**isamplegrabber**](isamplegrabber.md).

## <a name="members"></a>Member

Die **isamplegrabbercb** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Isamplegrabbercb** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **isamplegrabbercb** -Schnittstelle verfügt über diese Methoden.



| Methode                                        | BESCHREIBUNG                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**Buffercb**](isamplegrabbercb-buffercb.md) | Rückruf Methode, die einen Zeiger auf den Beispiel Puffer empfängt.<br/> |
| [**Samplecb**](isamplegrabbercb-samplecb.md) | Rückruf Methode, die einen Zeiger auf das Medien Beispiel empfängt.<br/>  |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



 

 
