---
description: Um zu bestimmen, ob ein Sicherheitsdeskriptor self-relative oder absolute ist, rufen Sie die GetSecurityDescriptorControl-Funktion auf, und überprüfen Sie die SE \_ SELF \_ RELATIVE-Flag des SECURITY \_ DESCRIPTOR \_ CONTROL-Parameters.
ms.assetid: dab2844b-7df9-446c-aacf-380a0a805cbc
title: Absolute und Self-Relative-Sicherheitsbeschreibungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a2639d1f17527b92116eabcaca96b637012253bbafc42198e37c9867fc585c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914722"
---
# <a name="absolute-and-self-relative-security-descriptors"></a>Absolute und Self-Relative-Sicherheitsbeschreibungen

Eine [*Sicherheitsbeschreibung*](/windows/desktop/SecGloss/s-gly) kann entweder im [*absoluten*](/windows/desktop/SecGloss/a-gly) oder [*im selbstbezogenen*](/windows/desktop/SecGloss/s-gly) Format vorliegen. Im absoluten Format enthält ein Sicherheitsdeskriptor Zeiger auf seine Informationen, nicht auf die Informationen selbst. Im selbstbezogenen Format speichert ein Sicherheitsdeskriptor eine [**SECURITY \_ DESCRIPTOR-Struktur**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) und die zugehörigen Sicherheitsinformationen in einem zusammenhängenden Speicherblock. Um zu bestimmen, ob ein Sicherheitsdeskriptor self-relative oder absolute ist, rufen Sie die [**GetSecurityDescriptorControl-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) auf, und überprüfen Sie das SE \_ SELF \_ RELATIVE-Flag des [**SECURITY \_ DESCRIPTOR \_ CONTROL-Parameters.**](security-descriptor-control.md) Sie können die Funktionen [**MakeSelfRelativeSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeselfrelativesd) und [**MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd) zum Konvertieren zwischen diesen beiden Formaten verwenden.

Das absolute Format ist nützlich, wenn Sie einen Sicherheitsdeskriptor erstellen und Zeiger auf alle Komponenten haben, z. B. wenn Standardeinstellungen für den Besitzer, die Gruppe und die diskrete ACL verfügbar sind. In diesem Fall können Sie die [**InitializeSecurityDescriptor-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) aufrufen, um eine [**SECURITY \_ DESCRIPTOR-Struktur**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) zu initialisieren, und dann Funktionen wie [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) aufrufen, um dem Sicherheitsdeskriptor ACL- und SID-Zeiger zuzuweisen.

Im selbstbezogenen Format beginnt ein Sicherheitsdeskriptor immer mit einer [**SECURITY \_ DESCRIPTOR-Struktur,**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) aber die anderen Komponenten des Sicherheitsdeskriptors können der Struktur in beliebiger Reihenfolge folgen. Anstatt Speicheradressen zu verwenden, werden die Komponenten des Sicherheitsdeskriptors durch Offsets vom Anfang des Deskriptors identifiziert. Dieses Format ist nützlich, wenn ein Sicherheitsdeskriptor auf dem Datenträger gespeichert, mithilfe eines Kommunikationsprotokolls übertragen oder in den Arbeitsspeicher kopiert werden muss.

Mit Ausnahme von [**MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd)verwenden alle Funktionen, die einen Sicherheitsdeskriptor zurückgeben, das selbst relative Format. Sicherheitsbeschreibungen, die als Argumente an eine Funktion übergeben werden, können entweder selbst relativ oder absolut sein. Weitere Informationen finden Sie in der Dokumentation für die Funktion.

 

 
