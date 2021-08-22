---
title: Zeichenfolgen im C-Format
description: Eine WinSNMP-Anwendung kann NULL-terminierte Zeichenfolgen im C-Stil verwenden, um Entitäts- und Objektbezeichnerobjekte (OID) in und aus ihren Zeichenfolgendarstellungen zu konvertieren.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6449514d4c08baae638d950a42f7f553e0037efe6bdc45b8045dbd315c1a2c65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009749"
---
# <a name="c-style-strings"></a>Zeichenfolgen im C-Format

Eine WinSNMP-Anwendung kann NULL-terminierte Zeichenfolgen im C-Stil verwenden, um Entitäts- und Objektbezeichnerobjekte (OID) in und aus ihren Zeichenfolgendarstellungen zu konvertieren.

Zu den WinSNMP-Funktionen, die Zeichenfolgen im C-Stil bearbeiten, gehören [**SnmpStrToEntity,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) [**SnmpEntityToStr,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)und [**SnmpOidToStr.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) Da [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) und [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) einen Zeiger auf eine Zeichenfolgenvariable im C-Stil zurückgeben, muss die WinSNMP-Anwendung beim Aufrufen dieser Funktionen einen entsprechenden Wert im *Size-Parameter* übergeben. Weitere Informationen finden Sie auf den Referenzseiten für diese Funktionen.

> [!Note]  
> Der *Kontextparameter* der Funktionen [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) und [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) muss eine Oktettzeichenfolgenstruktur sein, d. h. eine [**smiOCTETS-Struktur.**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) Der *Kontextparameter* darf keine Zeichenfolge im C-Stil sein. Die in einer **smiOCTETS-Struktur** enthaltene Zeichenfolge erfordert kein **Byte** mit NULL-Abbruch.

 

 

 




