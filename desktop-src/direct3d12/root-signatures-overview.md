---
title: Übersicht über Stamm Signaturen
description: Eine Stamm Signatur wird von der APP und Verknüpfungen Befehlslisten mit den Ressourcen konfiguriert, die für die Shader erforderlich sind.
ms.assetid: 2E649DA2-6CAC-4C2A-A420-D4EC0DD6EA73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85eb5882e4a893c2933c55281f21c49f2d7d50d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548707"
---
# <a name="root-signatures-overview"></a>Übersicht über Stamm Signaturen

Eine Stamm Signatur wird von der APP und Verknüpfungen Befehlslisten mit den Ressourcen konfiguriert, die für die Shader erforderlich sind. Die Grafik Befehlsliste verfügt sowohl über eine Grafik als auch über eine COMPUTE-Stamm Signatur. Eine COMPUTE-Befehlsliste hat einfach nur eine computestammsignatur. Diese Stamm Signaturen sind voneinander unabhängig.

-   [Stamm Parameter und Argumente](#root-parameters-and-arguments)
-   [Stamm Konstanten, Deskriptoren und Tabellen](#root-constants-descriptors-and-tables)
-   [Verwandte Themen](#related-topics)

## <a name="root-parameters-and-arguments"></a>Stamm Parameter und Argumente

Eine Stamm **Signatur** ähnelt einer API-Funktions Signatur, Sie bestimmt die Typen von Daten, die von den Shadern erwartet werden, aber definiert nicht den tatsächlichen Arbeitsspeicher oder die tatsächlichen Daten. Ein **Root-Parameter** ist ein Eintrag in der Stamm Signatur. Die tatsächlichen Werte der Stamm Parameter, die zur Laufzeit festgelegt und geändert werden, werden als Stamm **Argumente** bezeichnet. Durch das Ändern der Stamm Argumente werden die von den Shadern gelesenen Daten geändert.

## <a name="root-constants-descriptors-and-tables"></a>Stamm Konstanten, Deskriptoren und Tabellen

Die Stamm Signatur kann drei Typen von Parametern enthalten. Stamm Konstanten (in den root-Argumenten Inline-Konstanten), Stamm Deskriptoren (in den root-Argumenten Inline Deskriptoren) und deskriptortabellen (Zeiger auf einen Bereich von Deskriptoren im deskriptorheap).

Die Stamm Konstanten sind Inline-32-Bit-Werte, die im Shader als konstanter Puffer angezeigt werden.

Die Inline-root-Deskriptoren sollten Deskriptoren enthalten, auf die am häufigsten zugegriffen wird. Sie sind jedoch auf cbvs und RAW-oder strukturierte UAV-oder SRV-Puffer beschränkt. Ein komplexerer Typ, z. b. ein 2D-Textur-SRV, kann nicht als Stamm Deskriptor verwendet werden. Stamm Deskriptoren enthalten keine Größenbeschränkung. es kann also keine Überprüfung außerhalb der Grenzen erfolgen, anders als bei Deskriptoren in deskriptorheaps, die eine Größe enthalten.

Deskriptortabelleneinträge innerhalb von Stamm Signaturen enthalten den Deskriptor, den HLSL-Shader-Bindungs Namen und das Sichtbarkeits Kennzeichen. Weitere Informationen zu shadernamen finden Sie unter [Shader-Modell 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1) . Bei manchen Hardware kann es zu Leistungsvorteilen kommen, wenn Deskriptoren nur für die shaderphasen sichtbar gemacht werden müssen, die Sie benötigen (Weitere Informationen finden Sie unter [**D3D12 \_ Shader \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)).

![stammdeskriptortabelleneintrag](images/root-descriptor-table.png)

Das Layout der Stamm Signatur ist recht flexibel, wobei einige Einschränkungen auf weniger leistungsfähige Hardware angewendet werden. Unabhängig von der Hardwareebene sollten Anwendungen immer versuchen, die Stamm Signatur so klein wie erforderlich zu machen, um eine maximale Effizienz zu erzielen. Anwendungen können mit mehr deskriptortabellen in der Stamm Signatur, aber weniger Platz für Stamm Konstanten oder umgekehrt.

Der Inhalt der Stamm Signatur (die deskriptortabellen, Stamm Konstanten und Stamm Deskriptoren), die von der Anwendung gebunden wurden, wird vom D3D12-Treiber immer dann versioniert, wenn sich ein Teil der Inhalte zwischen Draw (graphics)/Dispatch (Compute)-aufrufen ändert. Jede Zeichnung/Dispatch erhält also einen eindeutigen vollständigen Stamm Signatur Zustand.

Im Idealfall gibt es Gruppen von Pipeline Zustands Objekten (PSOs), die dieselbe Stamm Signatur gemeinsam verwenden. Nachdem eine Stamm Signatur in der Pipeline festgelegt wurde, können alle Bindungen, die Sie definiert (deskriptortabellen, Deskriptoren, Konstanten), einzeln festgelegt oder geändert werden, einschließlich Vererbung in Bündel.

Eine APP kann einen eigenen Kompromiss zwischen der Anzahl der zu lesenden deskriptortabellen in Inline Deskriptoren machen (die mehr Platz beanspruchen, aber eine Dereferenzierung aufheben), die Inline Konstanten (ohne Dereferenzierung) in der Stamm Signatur. Anwendungen sollten die Stamm Signatur so sparsam wie möglich verwenden und sich auf den von der Anwendung kontrollierten Arbeitsspeicher verlassen, z. b. Heaps und deskriptorheaps, die auf Sie verweisen, um Massendaten darzustellen.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Stamm Signaturen](root-signatures.md)
</dt> </dl>

 

 