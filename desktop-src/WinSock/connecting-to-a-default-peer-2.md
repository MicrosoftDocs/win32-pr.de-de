---
description: Wspconnect richtet eine Standardziel Adresse ein, damit ein Socket mit nachfolgenden Sende-(wspsend) und Receive (wsprecv)-Vorgängen verwendet werden kann.
ms.assetid: efd57cb1-9736-4527-8e20-ab9304e3a8f6
title: Herstellen einer Verbindung mit einem standardpeer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22ca4aff0cdc8560459dd2571d79a71a85fcc71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345722"
---
# <a name="connecting-to-a-default-peer"></a>Herstellen einer Verbindung mit einem standardpeer

Bei einem Socket, der an ein verbindungsloses Protokoll gebunden ist, besteht der von [**wspconnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) ausgeführte Vorgang darin, nur eine Standardziel Adresse einzurichten, sodass der Socket mit nachfolgenden Verbindungs orientierten Sende-und Empfangs Vorgängen ([**wspsend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) und [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))) verwendet werden kann. Alle Datagramme, die von einer anderen Adresse als der angegebenen Zieladresse empfangen werden, werden verworfen.

 

 
