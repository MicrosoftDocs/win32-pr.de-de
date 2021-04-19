---
description: Der dispatchmapper wird mit com cokreateinstance erstellt und macht eine Schnittstelle, itdispatchmapper, verfügbar.
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Dispatchzuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed0a3a6cbc906861f5e95694bfd75aec6f5791f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349208"
---
# <a name="dispatch-mapper"></a>Dispatchzuordnung

Der dispatchmapper wird mit com **cokreateinstance** erstellt und macht eine Schnittstelle, [**itdispatchmapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper), verfügbar. Diese Schnittstelle ermöglicht es einer Anwendung, den Dispatch-Zeiger einer anderen Schnittstelle für ein Objekt abzurufen, wenn der Dispatch-Zeiger einer Schnittstelle und die GUID eines anderen Objekts ist. Diese Schnittstelle wird bereitgestellt, um Programmierer bei der Verwendung von Skript Anwendungen zu unterstützen, die keine Möglichkeit bieten, die Schnittstellen eines Objekts schnell abzufragen.

Der dispatchmapper verwendet die **iobjecgs** -Schnittstelle eines Objekts, um sicherzustellen, dass das Objekt für die Skripterstellung auf der angeforderten Schnittstelle sicher ist. Wenn das Objekt **iobjeczafety** nicht implementiert, oder wenn das Objekt an dieser speziellen Schnittstelle nicht sicher ist, tritt ein Fehler auf.

 

 



