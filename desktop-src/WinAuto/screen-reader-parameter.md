---
title: Sprachausgabeparameter
description: Der Sprachausgabeparameter gibt an, ob eine Anwendung Textinformationen in Situationen bereitstellen soll, in denen sie die Informationen andernfalls grafisch darstellen würde.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818ad36cfe833c1c9a3f39047cd88e6b4e8be55972d521ce524bb1e0618a48ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098420"
---
# <a name="screen-reader-parameter"></a>Sprachausgabeparameter

Der Sprachausgabeparameter gibt an, ob eine Anwendung Textinformationen in Situationen bereitstellen soll, in denen sie die Informationen andernfalls grafisch darstellen würde.

Dieser Parameter wird in der Regel durch Barrierefreiheitshilfen wie Sprachausgaben festgelegt. Anwendungen verwenden die **FLAGS SPI \_ GETSCREENREADER** und **SPI \_ SETSCREENREADER** mit der [**SystemParametersInfo-Funktion,**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) um den Sprachausgabeparameter abzurufen und festzulegen.

> [!Note]  
> Die Sprachausgabe, die in Windows enthaltene Sprachausgabe, legt die **FLAGS SPI \_ SETSCREENREADER** oder **SPI \_ GETSCREENREADER** nicht fest.

 

 

 