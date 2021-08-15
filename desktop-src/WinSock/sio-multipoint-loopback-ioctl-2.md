---
description: Verwenden des SIO \_ MULTIPOINT \_ LOOPBACK-Befehlscodes zum Aktivieren oder Deaktivieren des Loopbacks von Multipoint-Datenverkehr.
ms.assetid: 7e11932b-ce9a-4500-888f-8a08ab67b46c
title: SIO_MULTIPOINT_LOOPBACK Ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b75c781aeeaa67327dd2eaa57efb1eaccaf5d1d62daf3ffa9de3ce63fedbe2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097510"
---
# <a name="sio_multipoint_loopback-ioctl"></a>SIO \_ MULTIPOINT \_ LOOPBACK Ioctl

Wenn d \_ Blattsockets in einer nicht entrooteten Datenebene verwendet werden, ist es im Allgemeinen wünschenswert, steuern zu können, ob der gesendete Datenverkehr auch wieder auf demselben Socket empfangen wird. Der SIO \_ MULTIPOINT \_ LOOPBACK-Befehlscode für [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) wird verwendet, um loopback von Multipoint-Datenverkehr zu aktivieren oder zu deaktivieren.

 

 
