---
description: WMI unterstützt derzeit keinen verwalteten Code in WMI, wird aber in mi unterstützt.
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
ms.openlocfilehash: 6f28b01cb3b4506e0b47332cc3336af95dd641e78c7716f33b8e62b162081bdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071520"
---
# <a name="creating-a-managed-wmi-client"></a>Erstellen eines verwalteten WMI-Clients

Die aktuelle Version von WMI enthält den System.Management-Namespace, der eine Reihe von APIs verfügbar macht, die mit WMI interagieren. Es wird jedoch nicht empfohlen, diesen Namespace zu verwenden.

Wenn Sie einen verwalteten WMI-Client erstellen möchten, sollten Sie die Windows Management Infrastructure (MI) verwenden. MI ist die Version der nächsten Generation von WMI und enthält vollständige Unterstützung für verwalteten Code. Weitere Informationen finden Sie unter [Implementieren eines verwalteten MI-Clients.](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client)

 

 
