---
title: Die STGMEDIUM-Struktur
description: Die STGMEDIUM-Struktur
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86faf52ab93bab39b8413ea2eb6381da24b643b5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104039824"
---
# <a name="the-stgmedium-structure"></a>Die STGMEDIUM-Struktur

Ebenso wie die [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur eine Erweiterung des Windows-Zwischenablage-Format Bezeichners ist, ist die [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur eine Verbesserung des globalen Speicher Handles, das zum Übertragen der Daten verwendet wird. Die **STGMEDIUM** -Struktur schließt den Member, **TYMED**, ein, der das zu verwendende Medium angibt, und eine Union, die Zeiger und ein Handle für die Angabe des Mediums angibt, das in **TYMED** angegeben ist.

Die [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur ermöglicht es Datenquellen und Consumern, das effizienteste Exchange-Medium auf renderbasis auszuwählen. Wenn die Daten so umfangreich sind, dass Sie auf dem Datenträger aufbewahrt werden sollen, kann die Datenquelle ein Datenträger basiertes Medium in seinem bevorzugten Format angeben und nur globalen Speicher als eine Sicherung verwenden, wenn dies das einzige Medium ist, das der Consumer versteht. Wenn Sie das beste Medium für Austausch Vorgänge als Standard verwenden können, wird die Gesamtleistung des Datenaustauschs zwischen Anwendungen verbessert. Wenn z. b. einige der zu übertragenden Daten bereits auf dem Datenträger vorhanden sind, kann die Quell Anwendung Sie verschieben oder in ein neues Ziel kopieren, entweder in der gleichen Anwendung oder in anderen, ohne dass die Daten zuerst in den globalen Speicher geladen werden müssen. Am empfangenden Ende muss der Consumer der Daten nicht auf den Datenträger zurückgeschrieben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenformate und Übertragungsmedien](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




