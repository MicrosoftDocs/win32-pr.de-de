---
title: ITF contextrenderingmarkup-Schnittstelle
description: Die ITF contextrenderingmarkup-Schnittstelle wird von TSF Manager implementiert und von Anwendungen verwendet. Diese Schnittstelle kann mit iqueryinterface aus dem ITfContext-Objekt abgerufen werden. Diese Schnittstelle unterstützt die Anwendung beim Auflisten von Renderinginformationen.
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- ITF contextrenderingmarkup Interface Text Services-Framework
- ITF contextrenderingmarkup Interface Text Services-Framework, beschrieben
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b71e977665a4b3a6e817ef782ee558064e0986a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858341"
---
# <a name="itfcontextrenderingmarkup-interface"></a>ITF contextrenderingmarkup-Schnittstelle

Die **ITF contextrenderingmarkup** -Schnittstelle wird von TSF Manager implementiert und von Anwendungen verwendet. Diese Schnittstelle kann mit iqueryinterface aus dem [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) -Objekt abgerufen werden. Diese Schnittstelle unterstützt die Anwendung beim Auflisten von Renderinginformationen.



| ITF contextrenderingmarkup-Methoden                                                | BESCHREIBUNG                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md)           | Ruft einen Enumerator der rendermarkups für den angegebenen Bereich ab. |
| [Findnextrenderingmarkup](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | Diese Funktion ist nicht implementiert. Er gibt immer E \_ notimpl zurück.       |



 

## <a name="members"></a>Member

Die **itfcontextrenderingmarkup** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Diese Schnittstelle befindet sich derzeit nicht in den öffentlichen Header Dateien. Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.

 

 

 