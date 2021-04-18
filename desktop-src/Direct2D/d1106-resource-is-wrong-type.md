---
title: D1106 Ressource ist falsch.
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: Die angegebene Ressource weist nicht den erwarteten Typ auf.
keywords:
- D1106 Ressource hat den falschen Typ Direct2D
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5c38ef36319b8021de918a798c94a3be0683a7b7
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "106372019"
---
# <a name="d1106-resource-is-wrong-type"></a>D1106: Ressource ist falsch.

Die angegebene Ressourcen \[ *Ressource* weist \] nicht den erwarteten Typ auf.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Ressource*
</dt> <dd>

Die Adresse der Ressource.

</dd> </dl> 




 

## <a name="possible-causes"></a>Mögliche Ursachen

Eine Schnittstelle wurde nicht ordnungsgemäß umgewandelt und als Parameter für eine Methode oder Funktion verwendet.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Wert weitergeleitet, wenn ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) erwartet wird.


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



Dieses Beispiel erzeugt die folgende Debugmeldung:

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a>Fehlerbehebungen

Verwenden Sie den Typ, der von der Methode benötigt wird.

 

 
