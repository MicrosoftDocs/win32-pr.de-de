---
description: Der Installer legt Eigenschaften mit der folgenden Rangfolge fest. Ein Eigenschafts Wert in dieser Liste kann einen Wert, der darauf folgt, außer Kraft setzen und durch einen Wert überschrieben werden, der in der Liste vor ihm liegt.
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: Reihenfolge der Eigenschafts Rangfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366300"
---
# <a name="order-of-property-precedence"></a>Reihenfolge der Eigenschafts Rangfolge

Der Installer legt Eigenschaften mit der folgenden Rangfolge fest. Ein Eigenschafts Wert in dieser Liste kann einen Wert, der darauf folgt, außer Kraft setzen und durch einen Wert überschrieben werden, der in der Liste vor ihm liegt.

1.  Eigenschaften, die von der Betriebsumgebung festgelegt werden.
2.  [Öffentliche Eigenschaften](public-properties.md) , die in der Befehlszeile festgelegt werden.
3.  Öffentliche Eigenschaften, die während einer [administrativen Installation](administrative-installation.md) durch das [**Eigenschaftenset adminproperties**](adminproperties.md) aufgelistet werden.
4.  Öffentliche oder private Eigenschaften, die während der Anwendung einer [*Transformation*](t-gly.md)festgelegt werden.
5.  Eine öffentliche oder private Eigenschaft, die durch das Erstellen der [Eigenschaften Tabelle](property-table.md) der MSI-Datei festgelegt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> </dl>

 

 



