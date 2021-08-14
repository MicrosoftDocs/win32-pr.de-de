---
description: Ein gültiger funktionaler Sicherheitsdeskriptor enthält Sicherheitsinformationen im Binärformat.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Sicherheitsbeschreibungszeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbefeb87a7fca30f0c33d6f180315df5e5d576dc018e69dc680391050a840d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413790"
---
# <a name="security-descriptor-strings"></a>Sicherheitsbeschreibungszeichenfolgen

Ein gültiger funktionaler [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly) enthält Sicherheitsinformationen im Binärformat. Die Windows-API stellt Funktionen zum Konvertieren binärer Sicherheitsbeschreibungen in und aus Textzeichenfolgen bereit. Sicherheitsbeschreibungen im Zeichenfolgenformat sind nicht funktionsfähig, können aber nützlich sein, um Sicherheitsbeschreibungsinformationen zu speichern oder zu übertragen.

Um einen Sicherheitsdeskriptor in ein Zeichenfolgenformat zu konvertieren, rufen Sie die [**ConvertSecurityDescriptorToStringSecurityDescriptor-Funktion**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) auf. Um einen Sicherheitsdeskriptor im Zeichenfolgenformat zurück in einen gültigen funktionalen Sicherheitsdeskriptor zu konvertieren, rufen Sie die [**ConvertStringSecurityDescriptorToSecurityDescriptor-Funktion**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) auf.

Weitere Informationen finden Sie unter [Sicherheitsbeschreibungsdefinitionssprache](security-descriptor-definition-language.md).

 

 
