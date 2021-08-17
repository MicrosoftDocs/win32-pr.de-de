---
title: Der ACF-Header
description: Der ACF-Header enthält plattformspezifische Attribute, die für die Schnittstelle als Ganzes gelten. Attribute, die auf einzelne Typen und Funktionen im ACF-Text angewendet werden, überschreiben die Attribute im ACF-Header. Im ACF-Header sind keine Attribute erforderlich.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdfeced843337143fd441d816e3b575be2e7ebc7d93000094f8dcd3737a00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924610"
---
# <a name="the-acf-header"></a>Der ACF-Header

Der ACF-Header enthält plattformspezifische Attribute, die für die Schnittstelle als Ganzes gelten. Attribute, die auf einzelne Typen und Funktionen im ACF-Text angewendet werden, überschreiben die Attribute im ACF-Header. Im ACF-Header sind keine Attribute erforderlich.

Der ACF-Header kann eines der folgenden Attribute enthalten: **\[** [**\_ automatisches**](/windows/desktop/Midl/auto-handle) **\]** Handle, implizites Handle oder **\[** [**\_**](/windows/desktop/Midl/implicit-handle) **\]** [**explizites \_ Handle.**](/windows/desktop/Midl/explicit-handle) **\]** Wenn **\[ auto handle \_ oder \]** **\[ implicit \_ handle \]** verwendet wird, gibt es den Typ des Bindungshandpunkts an, der für die Bindung verwendet wird, wenn eine Remotefunktion keinen expliziten Bindungshand handle-Parameter hat. Wenn der ACF nicht vorhanden ist oder kein automatisches, implizites oder explizites Bindungshandle an gibt, verwendet MIDL **\[ \_ \]** das automatische Handle für die implizite Bindung.

Entweder **\[** [**Code oder**](/windows/desktop/Midl/code) **\]** **\[** [**Nocode**](/windows/desktop/Midl/nocode) kann im Schnittstellenheader angezeigt werden, aber der von Ihnen wähle **\]** kann nur einmal angezeigt werden. Wenn kein Attribut vorhanden ist, verwendet der Compiler **\[ Code \]** als Standard.

Weitere Informationen finden Sie unter [ACF-Attribute.](/windows/desktop/Midl/acf-attributes)

 

 