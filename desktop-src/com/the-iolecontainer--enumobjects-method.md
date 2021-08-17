---
title: Die IOleContainer EnumObjects-Methode
description: Die IOleContainer EnumObjects-Methode
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbd74e4916eec4d58240f702a09fd8376008fe0bb352113e1512bd2882d8dee9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462320"
---
# <a name="the-iolecontainerenumobjects-method"></a>Die IOleContainer::EnumObjects-Methode

Diese Methode wird verwendet, um alle OLE-Objekte aufzuzählen, die in einem Dokument oder Formular enthalten sind, und gibt einen Schnittstellenzeiger für jedes OLE-Objekt zurück. Der Container muss Zeiger auf jedes OLE-Objekt zurückgeben, das denselben Container gemeinsam verwendet. Geschachtelte Formulare oder geschachtelte Steuerelemente müssen ebenfalls aufzählt werden.

Einige Container implementieren Extendersteuerelemente, die Nicht-ActiveX-Steuerelemente umschließen und dann Zeiger auf diese Extendersteuerelemente zurückgeben, wenn ein Formular aufzählt wird. Dieses Verhalten ermöglicht es ActiveX Steuerelementen und ActiveX Steuerelementcontainern, sich gut in Nicht-ActiveX-Steuerelemente zu integrieren. Daher wird empfohlen, aber nicht erforderlich.

 

 




