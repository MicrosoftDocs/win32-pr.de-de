---
description: Die IAMSetErrorLog-Schnittstelle legt ein Fehlerprotokoll in DirectShow Editing Services (DES) fest oder ruft es ab.
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: IAMSetErrorLog-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8a16e56de7f350b30c1b92c0c94ff3e3e06afc31b363c0b3a6e98017ce483aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756400"
---
# <a name="iamseterrorlog-interface"></a>IAMSetErrorLog-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `IAMSetErrorLog` Schnittstelle legt ein Fehlerprotokoll in [DirectShow Editing Services](directshow-editing-services.md) (DES) fest oder ruft es ab. Das Zeitachsenobjekt implementiert diese Schnittstelle. Anwendungen können diese Schnittstelle verwenden, um Renderingfehler zur Laufzeit zu protokollieren. Implementieren Sie [**die IAMErrorLog-Schnittstelle**](iamerrorlog.md) in Ihrer Anwendung, und rufen Sie dann die [**IAMSetErrorLog::p ut \_ ErrorLog-Methode**](iamseterrorlog-put-errorlog.md) auf der Zeitachse auf.

Weitere Informationen zur Verwendung dieser Schnittstelle finden Sie unter [Protokollierungsfehler.](logging-errors.md)

## <a name="members"></a>Member

Die **IAMSetErrorLog-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMSetErrorLog** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAMSetErrorLog-Schnittstelle** verfügt über diese Methoden.



| Methode                                               | Beschreibung                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [**Get \_ ErrorLog**](iamseterrorlog-get-errorlog.md) | Ruft das aktuelle Fehlerprotokoll für dieses Objekt ab.<br/> |
| [**put \_ ErrorLog**](iamseterrorlog-put-errorlog.md) | Gibt ein Fehlerprotokoll für das -Objekt an.<br/>           |



 

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



 

 
