---
description: Sowohl Client- als auch Serverzertifikate müssen in einem Zertifikatspeicher gespeichert werden, auf den der Anwendungsprozess zugreifen kann.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Zertifikatspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64451ea7f568bb5e86289d5d9f1587d98b65aa1d53c14a4a251a5e61fe72b21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883490"
---
# <a name="certificate-stores"></a>Zertifikatspeicher

Sowohl [*Client-*](/windows/desktop/SecGloss/c-gly) als [*auch Serverzertifikate*](/windows/desktop/SecGloss/s-gly) müssen in einem Zertifikatspeicher gespeichert werden, auf den [*der*](/windows/desktop/SecGloss/c-gly) Anwendungsprozess zugreifen kann. In der Regel ist dies der My Store, der auch als persönlicher Speicher bezeichnet wird. Clientanwendungen wie Internet Explorer verwenden normalerweise den My-Speicher des aktuellen Benutzers, während Server wie Internetinformationsdienste (IIS) das System My store des lokalen Computers verwenden.

Der Stammspeicher und der [*Zertifizierungsstellenspeicher*](/windows/desktop/SecGloss/c-gly) werden verwendet, wenn Schannel oder eine Anwendung eine Zertifikatkette erstellt, die an den Remotecomputer gesendet werden soll. Diese Speicher werden verwendet, um eine empfangene Zertifikatkette zu überprüfen. Weitere Informationen finden Sie unter [Durchführen der Authentifizierung mit Schannel](performing-authentication-using-schannel.md).

 

 
