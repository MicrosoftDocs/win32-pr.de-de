---
title: Bildschirm Lese Parameter
description: Der Bildschirm Lese Parameter gibt an, ob eine Anwendung Textinformationen in Situationen bereitstellen soll, in denen Sie die Informationen andernfalls grafisch darstellen würde.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c237f3d945b9782884ffc655cf87a203159a16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039262"
---
# <a name="screen-reader-parameter"></a>Bildschirm Lese Parameter

Der Bildschirm Lese Parameter gibt an, ob eine Anwendung Textinformationen in Situationen bereitstellen soll, in denen Sie die Informationen andernfalls grafisch darstellen würde.

Dieser Parameter wird in der Regel durch Barrierefreiheits Hilfen wie Bildschirm Sprachausgaben festgelegt. Anwendungen verwenden die **SPI \_ getscreenreader** -und **SPI \_ setscreenreader** -Flags mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um den Screenreader-Parameter zu erhalten und festzulegen.

> [!Note]  
> Die Sprachausgabe, die in Windows enthalten ist, legt die **SPI- \_ setscreenreader** -oder **SPI \_ getscreenreader** -Flags nicht fest.

 

 

 