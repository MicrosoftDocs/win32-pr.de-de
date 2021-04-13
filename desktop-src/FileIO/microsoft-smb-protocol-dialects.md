---
description: Zum Herstellen einer Verbindung zwischen einem Client und einem Server mithilfe des Microsoft SMB-Protokolls müssen Sie zunächst den Dialekt mit dem höchsten Grad an Funktionalität ermitteln, die sowohl vom Client als auch vom Server unterstützt werden.
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Microsoft SMB-Protokoll Dialekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484731"
---
# <a name="microsoft-smb-protocol-dialects"></a>Microsoft SMB-Protokoll Dialekte

Die Liste der Microsoft SMB-Protokollnachrichten Pakete ist im Laufe der Jahre gewachsen, um die zunehmende Funktionalität des Microsoft SMB-Protokolls und nun die Anzahl der Hunderte zu erfüllen. Jede Phase ihrer Vergrößerung wird durch einen Standardpaket Satz oder einen Dialekt gekennzeichnet. Jeder Dialekt wird durch eine Standard Zeichenfolge identifiziert, z. b. "PC-Netzwerkprogramm 1,0", "Microsoft Networks 3,0", "DOS LanMan 2,1" oder "NT LM 0,12". Die erste Zeichenfolge identifiziert den ersten Dialekt von SMB, und die letzte Zeichenfolge identifiziert CIFS, den ersten Dialekt des Microsoft SMB-Protokolls.

Die meisten Windows-Clients unterstützen mindestens sechs verschiedene Dialekte des Microsoft SMB-Protokolls. Daher besteht einer der ersten Schritte beim Herstellen einer Verbindung zwischen einem Client und einem Server mithilfe des Microsoft SMB-Protokolls darin, den Dialekt mit dem höchsten Grad an Funktionalität zu ermitteln, die sowohl vom Client als auch vom Server unterstützt werden. Dieser Prozess wird als "Aushandeln des Dialekts" bezeichnet. Die oben erwähnten Dialekt Zeichenfolgen sind zu diesem Zweck in den Dialekt Aushandlungs-Anforderungs-und Antwortpaketen enthalten.

 

 



