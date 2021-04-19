---
description: Die iamseterrorlog-Schnittstelle legt ein Fehlerprotokoll in DirectShow-Bearbeitungs Diensten fest oder ruft es ab.
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Iamenterrorlog-Schnittstelle (qedit. h)
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
ms.openlocfilehash: c0a24d29625bf08bc2f4c728a61f5188e8bec211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366972"
---
# <a name="iamseterrorlog-interface"></a>Iameinterrorlog-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IAMSetErrorLog` Schnittstelle legt ein Fehlerprotokoll in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) fest oder ruft es ab. Das Zeitachsen Objekt implementiert diese Schnittstelle. Anwendungen können diese Schnittstelle zum Protokollieren von renderingfehlern zur Laufzeit verwenden. Implementieren Sie die [**iamerrorlog**](iamerrorlog.md) -Schnittstelle in der Anwendung, und nennen Sie dann die Methode [**iamseterrorlog::p UT \_ ErrorLog**](iamseterrorlog-put-errorlog.md) auf der Zeitachse.

Weitere Informationen zur Verwendung dieser Schnittstelle finden Sie unter [Protokollieren von Fehlern](logging-errors.md).

## <a name="members"></a>Member

Die **iameinterrorlog** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamenterrorlog** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iameinterrorlog** -Schnittstelle verfügt über diese Methoden.



| Methode                                               | BESCHREIBUNG                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [**\_ErrorLog erhalten**](iamseterrorlog-get-errorlog.md) | Ruft das aktuelle Fehlerprotokoll für dieses-Objekt ab.<br/> |
| [**\_ErrorLog ablegen**](iamseterrorlog-put-errorlog.md) | Gibt ein Fehlerprotokoll für das-Objekt an.<br/>           |



 

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



 

 
