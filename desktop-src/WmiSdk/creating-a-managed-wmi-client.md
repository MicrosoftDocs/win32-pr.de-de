---
description: WMI unterstützt derzeit keinen verwalteten Code in WMI, wird jedoch in Mi unterstützt.
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: Erstellen eines verwalteten WMI-Clients
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb1339347c4e15cd29ebf4d4e98e5a8b61a24e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372978"
---
# <a name="creating-a-managed-wmi-client"></a>Erstellen eines verwalteten WMI-Clients

Die aktuelle Version von WMI enthält den System. Management-Namespace, der eine Reihe von APIs zur Verfügung stellt, die mit WMI interagieren. Es wird jedoch nicht empfohlen, diesen Namespace zu verwenden.

Wenn Sie einen verwalteten WMI-Client erstellen möchten, empfiehlt es sich, die Windows-Verwaltungsinfrastruktur (Mi) zu verwenden. Mi ist die Version von WMI der nächsten Generation und enthält vollständige Unterstützung für verwalteten Code. Weitere Informationen finden Sie unter [Implementieren eines verwalteten Mi-Clients](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).

 

 
