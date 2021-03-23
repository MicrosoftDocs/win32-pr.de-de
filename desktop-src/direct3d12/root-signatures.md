---
title: Stamm Signaturen
description: Die Stamm Signatur definiert, welche Typen von Ressourcen an die Grafik Pipeline gebunden sind.
ms.assetid: ee32a222-8469-4af5-b688-afa70cf77c6a
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4c034e208dd841545777cc92878e7020b9b4a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548701"
---
# <a name="root-signatures"></a>Stamm Signaturen

Die Stamm Signatur definiert, welche Typen von Ressourcen an die Grafik Pipeline gebunden sind.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                               | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Übersicht über Stamm Signaturen](root-signatures-overview.md)<br/>                                                 | Eine Stamm Signatur wird von der APP und Verknüpfungen Befehlslisten mit den Ressourcen konfiguriert, die für die Shader erforderlich sind. Die Grafik Befehlsliste verfügt sowohl über eine Grafik als auch über eine COMPUTE-Stamm Signatur. Eine COMPUTE-Befehlsliste hat einfach nur eine computestammsignatur. Diese Stamm Signaturen sind voneinander unabhängig.<br/>                                                                                             |
| [Verwenden einer Stamm Signatur](using-a-root-signature.md)<br/>                                                     | Bei der Stamm Signatur handelt es sich um die Definition einer beliebig angeordneten Auflistung von deskriptortabellen (einschließlich Layout), Stamm Konstanten und Stamm Deskriptoren. Jeder Eintrag hat einen Kosten Wert für eine Obergrenze, sodass die Anwendung das Gleichgewicht zwischen der Anzahl der einzelnen Eintrags Typen, die die Stamm Signatur enthalten wird, abwägen kann.<br/>                                                                     |
| [Erstellen einer Stamm Signatur](creating-a-root-signature.md)<br/>                                               | Stamm Signaturen sind eine komplexe Datenstruktur, die Struktur-Strukturen enthält. Diese können Programm gesteuert mithilfe der unten stehenden Datenstruktur Definition definiert werden (die Methoden zum Initialisieren von Membern umfasst). Alternativ dazu können Sie in High Level Shading Language (HLSL) erstellt werden, was den Vorteil bietet, dass der Compiler frühzeitig überprüft, ob das Layout mit dem Shader kompatibel ist. <br/> |
| [Stamm Signatur Limits](root-signature-limits.md)<br/>                                                       | Bei der Stamm Signatur handelt es sich um Primzahlen, und es sind strikte Grenzwerte und Kosten zu beachten.<br/>                                                                                                                                                                                                                                                                                                            |
| [Direkte Verwendung von Konstanten in der Stamm Signatur](using-constants-directly-in-the-root-signature.md)<br/>     | Anwendungen können Stamm Konstanten in der Stamm Signatur definieren, jeweils als Satz von 32-Bit-Werten. Sie werden in High Level Shading Language (HLSL) als konstanter Puffer angezeigt. Beachten Sie, dass Konstante Puffer aus historischen Gründen als Sätze von 4x32-Bit-Werten angezeigt werden. <br/>                                                                                                                                        |
| [Verwenden von Deskriptoren direkt in der Stamm Signatur](using-descriptors-directly-in-the-root-signature.md)<br/> | Anwendungen können Deskriptoren direkt in die Stamm Signatur einfügen, um zu vermeiden, dass Sie einen deskriptorheap durchlaufen müssen. Diese Deskriptoren belegen viel Platz in der Stamm Signatur (siehe den Abschnitt root Signature Limits), sodass Anwendungen Sie sparsam verwenden müssen. <br/>                                                                                                                                     |
| [Beispiel Stamm Signaturen](example-root-signatures.md)<br/>                                                   | Der folgende Abschnitt zeigt die Stamm Signaturen, die bei der Komplexität variieren, von leer bis vollständig.<br/>                                                                                                                                                                                                                                                                                                       |
| [Angeben von Stamm Signaturen in HLSL](specifying-root-signatures-in-hlsl.md)<br/>                             | Das Angeben von Stamm Signaturen im HLSL-Shader-Modell 5,1 ist eine Alternative zur Angabe in C++-Code.<br/>                                                                                                                                                                                                                                                                                                  |
| [Stamm Signatur Version 1,1](root-signature-version-1-1.md)<br/>                                             | Der Zweck der Stamm Signatur Version 1,1 besteht darin, dass Anwendungen den Treibern zeigen können, wenn sich die Deskriptoren in einem deskriptorheap geändert haben oder die Daten Deskriptoren auf die geänderte Änderung zeigen. Dies ermöglicht es der Option für Treiber, Optimierungen zu erstellen, bei denen möglicherweise ein Deskriptor oder der Arbeitsspeicher, auf den er verweist, für einen bestimmten Zeitraum statisch ist. <br/>                                  |



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> <dt>

[**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer)
</dt> <dt>

[Ressourcen Bindung](resource-binding.md)
</dt> </dl>

 

