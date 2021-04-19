---
title: COM-Handler
description: Der Zweck von com-Handlern ist die Angabe von \ 0034; Intelligent \ 0034; Code im Client Adressraum, der Aufrufe zwischen einem Client und einem Server optimieren kann. Handler können einige Schnittstellen überschreiben und andere direkt an den Server delegieren (über den Proxy).
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb66a94942cd46424339cfffbde925f62e20e5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341832"
---
# <a name="com-handlers"></a>COM-Handler

Der Zweck von com-Handlern besteht darin, einen "intelligenten" Code im Client Adressraum bereitzustellen, der Aufrufe zwischen einem Client und einem Server optimieren kann. Handler können einige Schnittstellen überschreiben und andere direkt an den Server delegieren (über den Proxy).

Es gibt zwei Arten von com-Handlern:

-   [Der OLE-Handler](the-ole-handler.md) ist eine umfangreich-dll, die wichtige Dienste zum Verknüpfen und Einbetten bereitstellt. Sie wird in der Regel vor dem Starten des Servers erstellt und initialisiert, sodass der Server aktiviert wird, wenn das eingebettete Objekt in den Zustand wird ausgeführt wechselt.
-   [Der Lightweight-Client seitige Handler](the-lightweight-client-side-handler.md) kann für beliebige Zwecke erstellt werden, kann sehr klein sein und kann nicht vor dem Server erstellt werden.

 

 




