---
title: Prozedur Format Zeichenfolgen
description: Im folgenden finden Sie eine ausführliche Beschreibung der Format Zeichenfolge. Es assembliert alle Ebenen, die mit verschiedenen Phasen der interpreterentwicklung verknüpft sind.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e58a9acf10caad23063bdba117dc402e411638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948976"
---
# <a name="procedure-format-strings"></a>Prozedur Format Zeichenfolgen

Im folgenden finden Sie eine ausführliche Beschreibung der Format Zeichenfolge. Es assembliert alle Ebenen, die mit verschiedenen Phasen der interpreterentwicklung verknüpft sind.

## <a name="procedure-descriptor-overview"></a>Übersicht über den Prozedur Deskriptor

Ein Prozedur Deskriptor besteht aus den Header Deskriptoren und den Parameter Deskriptoren. Die Beschreibung des [**– Oi**](/windows/desktop/Midl/-oi) -Stils wird in Bezug auf die allgemeine Verwendung in der aktuellen RPC-Programmierung als veraltet eingestuft. **– OIF** gilt als aktueller.

## <a name="the-oi-style-description"></a>Die Beschreibung des – Oi-Stils

Diese Beschreibung besteht aus den folgenden Elementen:

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

Der-Header würde zwischen 6 und 16 Bytes umfassen.

Die gesamte Beschreibung wird generiert, wenn im [**– Oi**](/windows/desktop/Midl/-oi) -Modus kompiliert wird. Im [**– OS**](/windows/desktop/Midl/-os) -Modus werden nur die Parameter Deskriptoren generiert, die für die Konvertierung verwendet werden. Der Pick-Interpreter verwendet alte Stil Parameter Deskriptoren.

## <a name="the-oif-style-description"></a>Die Beschreibung des – OIF-Stils

Die Beschreibung besteht aus den folgenden Elementen:

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

Der Header Deskriptor des [**– OIF**](/windows/desktop/Midl/-oi) -Stils besteht aus

Die Beschreibung des – OIF-Stils wird generiert, wenn im [**– OIF**](/windows/desktop/Midl/-oi) -oder **– Oicf** -Modus des Compilers kompiliert wird.

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

Einige neuere Features wie Pipe, Async und [**/robust**](/windows/desktop/Midl/-robust) erzwingen den [**– Oicf**](/windows/desktop/Midl/-oi) -Modus des Compilers, wenn er verwendet wird.

## <a name="the-extended-oif-description"></a>Die erweiterte –-OIF-Beschreibung

Die Beschreibung besteht aus den folgenden Elementen:

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 