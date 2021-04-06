---
title: Implementierung von irootstorage-Verbund Dateien
description: Die Implementierung der Verbund Datei von com in irootstorage ermöglicht Ihnen das Speichern von Dateien in Situationen mit geringem Arbeitsspeicher oder geringem Speicherplatz. Informationen dazu, wie sich diese Schnittstelle verhält, finden Sie unter irootstorage.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- Irootstorage-Erweiterung "STG", Implementierung von Verbund Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714568"
---
# <a name="irootstorage---compound-file-implementation"></a>Implementierung von irootstorage-Verbund Dateien

Die Implementierung der Verbund Datei von com in [**irootstorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) ermöglicht Ihnen das Speichern von Dateien in Situationen mit geringem Arbeitsspeicher oder geringem Speicherplatz. Informationen dazu, wie sich diese Schnittstelle verhält, finden Sie unter **irootstorage**.

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Verwenden Sie die vom System bereitgestellte Implementierung von [**irootstorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) nur, um das Speichern von Dateien unter einem Mangel an Arbeitsspeicher zu unterstützen.

## <a name="remarks"></a>Bemerkungen

Es ist möglich, die com-Implementierung von [**irootstorage:: switchdefile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) aufzurufen, um einen normalen Speicherungs Vorgang in einer anderen Datei durchzuführen. Anwendungen, die dies tun, sind jedoch möglicherweise nicht mit zukünftigen Generations Generationen des com-Speichers kompatibel. Um diese Möglichkeit zu vermeiden, sollten Anwendungen, die einen Save-as-Vorgang ausführen, die zweite Verbund Datei manuell erstellen und [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)aufrufen. Die **irootstorage:: switchdefile** -Methode sollte nur in Notfällen (wenig Arbeitsspeicher oder Speicherplatz) verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Irootstorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**Irootstorage:: SwitchTo-Datei**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




