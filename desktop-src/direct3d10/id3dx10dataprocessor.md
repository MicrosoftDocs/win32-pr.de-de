---
description: Datenverarbeitungs Objekt, das von der ID3DX10ThreadPump-Schnittstelle zum asynchronen verarbeiten geladener Daten verwendet wird.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: ID3DX10DataProcessor-Schnittstelle (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870212"
---
# <a name="id3dx10dataprocessor-interface"></a>ID3DX10DataProcessor-Schnittstelle

Datenverarbeitungs Objekt, das von der [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) zum asynchronen verarbeiten geladener Daten verwendet wird.

## <a name="members"></a>Member

Die **ID3DX10DataProcessor** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DX10DataProcessor** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10DataProcessor** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatedeviceobject"**](id3dx10dataprocessor-createdeviceobject.md) | Erstellen Sie ein Geräte Objekt.<br/>                                                                                                  |
| [**Zerstören**](id3dx10dataprocessor-destroy.md)                       | Wird von einer [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) verwendet, um den Prozessor zu zerstören, nachdem ein Arbeits Element abgeschlossen wurde.<br/> |
| [**Prozess**](id3dx10dataprocessor-process.md)                       | Verarbeiten einiger Daten.<br/>                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann geerbt und seine Member neu definiert werden. Auf diese Weise können Sie die API für die Verarbeitung Ihrer eigenen benutzerdefinierten Dateiformate anpassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
