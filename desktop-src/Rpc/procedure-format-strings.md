---
title: Prozedurformatzeichenfolgen
description: Es folgt eine vollständige Formatzeichenfolgenbeschreibung. Sie stellt alle Ebenen zusammen, die sich auf verschiedene Phasen der Interpreterentwicklung beziehen.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb17434a1c05b66212283237d61ee4492aa23ed0bf1ecca75f1fec1b3ddd784b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019058"
---
# <a name="procedure-format-strings"></a>Prozedurformatzeichenfolgen

Es folgt eine vollständige Formatzeichenfolgenbeschreibung. Sie stellt alle Ebenen zusammen, die sich auf verschiedene Phasen der Interpreterentwicklung beziehen.

## <a name="procedure-descriptor-overview"></a>Übersicht über den Prozedurdeskriptor

Ein Prozedurdeskriptor besteht aus den Headerdeskriptoren und den Parameterdeskriptoren. Die [**–Oi-Stilbeschreibung**](/windows/desktop/Midl/-oi) gilt im Hinblick auf die allgemeine Verwendung in der aktuellen RPC-Programmierung als veraltet. Der **-Oif** wird als aktueller betrachtet.

## <a name="the-oi-style-description"></a>Beschreibung des –Oi-Stils

Diese Beschreibung umfasst Folgendes:

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

Der Header hätte zwischen 6 und 16 Bytes.

Die vollständige Beschreibung wird beim Kompilieren im [**–Oi-Modus**](/windows/desktop/Midl/-oi) generiert. Im Modus [**"-Os"**](/windows/desktop/Midl/-os) werden nur die Parameterdeskriptoren generiert, die für die Konvertierung verwendet werden. Der Picklinginterpreter verwendet alte Stilparameterdeskriptoren.

## <a name="the-oif-style-description"></a>Beschreibung des –Oif-Stils

Die Beschreibung umfasst Folgendes:

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

Der [](/windows/desktop/Midl/-oi) -Oif-Stilheaderdeskriptor besteht aus

Die Beschreibung des -Oif-Stils wird beim Kompilieren im [**-Oif-**](/windows/desktop/Midl/-oi) oder **-Oicf-Modus** des Compilers generiert.

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

Einige neuere Features wie pipe, async und [**/robust**](/windows/desktop/Midl/-robust) erzwingen bei Verwendung den [**-Oicf-Modus**](/windows/desktop/Midl/-oi) des Compilers.

## <a name="the-extended-oif-description"></a>Die erweiterte Beschreibung von –Oif

Die Beschreibung umfasst Folgendes:

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 