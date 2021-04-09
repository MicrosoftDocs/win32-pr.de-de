---
title: Der ACF-Header
description: Der ACF-Header enthält plattformspezifische Attribute, die auf die gesamte Schnittstelle angewendet werden. Attribute, die auf einzelne Typen und Funktionen im ACF-Text angewendet werden, überschreiben die Attribute im ACF-Header. Im ACF-Header sind keine Attribute erforderlich.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e958044f043db8828f0fdda192918c632c321b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039269"
---
# <a name="the-acf-header"></a>Der ACF-Header

Der ACF-Header enthält plattformspezifische Attribute, die auf die gesamte Schnittstelle angewendet werden. Attribute, die auf einzelne Typen und Funktionen im ACF-Text angewendet werden, überschreiben die Attribute im ACF-Header. Im ACF-Header sind keine Attribute erforderlich.

Der ACF-Header kann eines der folgenden Attribute enthalten: **\[** [**Automatisches \_ handle**](/windows/desktop/Midl/auto-handle) **\]** , **\[** [**implizites \_**](/windows/desktop/Midl/implicit-handle)Handle **\]** oder [**explizites \_ handle**](/windows/desktop/Midl/explicit-handle) **\]** . Wenn ein **\[ Automatisches \_ handle \]** oder **\[ implizites \_ handle \]** verwendet wird, gibt es den Typ des Bindungs Handles an, der für die Bindung verwendet wird, wenn eine Remote Funktion keinen expliziten Bindungs handle-Parameter hat. Wenn die ACF nicht vorhanden ist oder kein automatisches, implizites oder explizites Bindungs Handle angibt, verwendet die Mittel l das **\[ automatische \_ handle \]** für die implizite Bindung.

Entweder **\[** kann [**Code**](/windows/desktop/Midl/code) **\]** oder **\[** [**NoCode**](/windows/desktop/Midl/nocode) **\]** im Schnittstellen Header angezeigt werden, aber der von Ihnen gewählte kann nur ein Mal angezeigt werden. Wenn keines der Attribute vorhanden ist, verwendet der Compiler **\[ Code \]** als Standardwert.

Weitere Informationen finden Sie unter [ACF-Attribute](/windows/desktop/Midl/acf-attributes).

 

 