---
title: D1009 Unerwarteter Hardwareerstellungsfehler
description: Beim Versuch, ein Direct3D-Ziel zu erstellen, ist ein unerwarteter Fehler \error\ aufgetreten.
ms.assetid: 1ff34b1f-0ab3-4821-97f5-a4e67831383a
keywords:
- D1009 Unerwarteter Hardwareerstellungsfehler Direct2D
topic_type:
- apiref
api_name:
- D1009 Unexpected Hardware Creation Error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa51d2536995feb51081134e412d94617f34d069
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548715"
---
# <a name="d1009-unexpected-hardware-creation-error"></a>D1009: Unerwarteter Hardwareerstellungsfehler

Unerwarteter \[ *Fehler* \] beim Erstellen eines Direct3D-Ziels.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="error"></span><span id="ERROR"></span>*Fehler*
</dt> <dd>

Eine Fehlernummer.

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Fehlerstufe | Warnung |



 

## <a name="possible-causes"></a>Mögliche Ursachen

-   Das Ziel war größer als die maximale Bitmapgröße.
-   Nicht genügend Videospeicher, wenn das Renderziel erstellt wird.
-   Es konnte kein Direct3D-Gerät erstellt werden.
-   Die Anwendung wird auf IA64 ausgeführt.

 

 




