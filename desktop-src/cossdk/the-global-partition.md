---
description: Die globale Partition
ms.assetid: db11e6f5-0a3d-44ce-9a51-90d7e2b80981
title: Die globale Partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc218067bbf7170a1c2df6f306b6dfe5787ac2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483862"
---
# <a name="the-global-partition"></a>Die globale Partition

Zusätzlich zu den vom Administrator definierten Partitionen und Partitions Sätzen ist auf jedem Computer, der als *globale Partition* bezeichnet wird, eine spezielle Partition vorhanden. Bei der Installation von com+ wird automatisch eine globale Partition erstellt. Die globale Partition ist so konzipiert, dass Sie systemweite Anwendungen enthält, die für alle Benutzer auf einem Server oder in der Domäne zugänglich sein müssen. Durch die Installation einer Anwendung in der globalen Partition entfällt die Notwendigkeit, eine Kopie der Anwendung in den Partitions Satz jedes einzelnen Benutzers zu installieren.

Wenn der Partitions Satz eines Benutzers keine bestimmte Anwendung enthält, auf die der Benutzer zugreifen möchte, aber diese Anwendung in der globalen Partition installiert ist, wird die Anwendung von der globalen Partition aus aktiviert. In diesem Fall müssen jedoch alle Komponenten der Anwendung, die in der globalen Partition installiert sind, als "Public", nicht als "private"-Komponenten gekennzeichnet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Standard Partitionen](default-partitions.md)
</dt> <dt>

[Lokale Partitionen](local-partitions.md)
</dt> <dt>

[Partitions Eigenschaften](partition-properties.md)
</dt> <dt>

[Partitionen und Active Directory](partitions-and-active-directory.md)
</dt> </dl>

 

 



