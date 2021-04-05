---
description: Client-und Server Zertifikate müssen in einem Zertifikat Speicher gespeichert werden, der für den Anwendungsprozess zugänglich ist.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Zertifikatspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042013"
---
# <a name="certificate-stores"></a>Zertifikatspeicher

[*Client*](/windows/desktop/SecGloss/c-gly) -und [*Server Zertifikate*](/windows/desktop/SecGloss/s-gly) müssen in einem [*Zertifikat Speicher*](/windows/desktop/SecGloss/c-gly) gespeichert werden, der für den Anwendungsprozess zugänglich ist. In der Regel ist dies der My-Speicher, der auch als persönlicher Speicher bezeichnet wird. Client Anwendungen, wie z. b. Internet Explorer, verwenden normalerweise den eigenen Speicher des aktuellen Benutzers, während Server wie Internetinformationsdienste (IIS) den systemeigenen Speicher des lokalen Computers verwenden.

Der Stamm Speicher und der [*Zertifizierungs*](/windows/desktop/SecGloss/c-gly) stellen Speicher werden verwendet, wenn SChannel oder eine Anwendung eine Zertifikat Kette erstellt, die an den Remote Computer gesendet werden soll. Diese Speicher werden verwendet, um eine empfangene Zertifikatskette zu überprüfen. Weitere Informationen finden Sie unter [Durchführen der Authentifizierung mithilfe von SChannel](performing-authentication-using-schannel.md).

 

 
