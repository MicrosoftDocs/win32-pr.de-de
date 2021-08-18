---
description: Die Dienstanbieter, die die Out-of-Band-Datenabstraktion (OOB) für die Sockets im Streamformat unterstützen, müssen der Semantik in diesem Abschnitt entsprechen.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Out-of-Band-Daten in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858e2845e9fbe198dc7af7a70edfad8a4ac429f8f1abe84289b87a779f6e478b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741050"
---
# <a name="out-of-band-data-in-the-spi"></a>Out-of-Band-Daten in der SPI

Die Dienstanbieter, die die Out-of-Band-Datenabstraktion (OOB) für die Sockets im Streamformat unterstützen, müssen der Semantik in diesem Abschnitt entsprechen. Die OOB-Datenverarbeitung wird protokollunabhängig beschrieben. Eine Erläuterung der OOB-Daten, die mit dringenden Daten in TCP/IP-Dienstanbietern implementiert wurden, finden Sie unter [Winsock-Dienstanbieter.](winsock-annexes.md) Im Folgenden gilt die Verwendung von [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) auch für [**WSPRecvFrom.**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))

 

 
