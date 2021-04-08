---
title: Zeichen folgen im C-Stil
description: Eine WinSNMP-Anwendung kann mit NULL endende Zeichen folgen im C-Stil zum Konvertieren von Entitäts-und objektbezeichnerobjekten (OID) in und aus ihren Zeichen folgen Darstellungen verwenden.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878398b6d8691982aa90b9f1376a38214030e52e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855215"
---
# <a name="c-style-strings"></a>Zeichen folgen im C-Stil

Eine WinSNMP-Anwendung kann mit **null** endende Zeichen folgen im C-Stil zum Konvertieren von Entitäts-und objektbezeichnerobjekten (OID) in und aus ihren Zeichen folgen Darstellungen verwenden.

Zu den WinSNMP-Funktionen, die Zeichen folgen im C-Stil bearbeiten, gehören [**snmpstreinentity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**snmpentitydestr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**snmpstrdeoid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)und [**snmpoiddestr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr). Da [**snmpentitydestr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) und [**snmpoidesstr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) einen Zeiger auf eine Zeichen folgen Variable im C-Format zurückgeben, muss die WinSNMP-Anwendung einen entsprechenden Wert im *size* -Parameter übergeben, wenn diese Funktionen aufgerufen werden. Weitere Informationen finden Sie auf den Referenzseiten für diese Funktionen.

> [!Note]  
> Der *Kontext* Parameter der [**snmpstrautcontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) -Funktion und der [**snmpcontextdestr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) -Funktion muss eine Oktett-Zeichen folgen Struktur sein, d. h. eine [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) -Struktur. Der *Kontext* Parameter darf keine Zeichenfolge im C-Format sein. Die in einer **smioctets** -Struktur enthaltene Zeichenfolge erfordert kein Byte, das **null** endet.

 

 

 




