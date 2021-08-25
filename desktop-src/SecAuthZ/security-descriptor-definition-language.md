---
description: Erläutert die SdDL (Security Descriptor Definition Language).
ms.assetid: 2b15325e-34ed-497b-ae6d-3ec3ac168232
title: Sicherheitsbeschreibungsdefinitionssprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b72e74f49d34577251aef3d875a3c0e9aede07556be1b918ad532f3987c54d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907410"
---
# <a name="security-descriptor-definition-language"></a>Sicherheitsbeschreibungsdefinitionssprache

Die SdDL (Security Descriptor Definition Language) definiert das Zeichenfolgenformat, das die Funktionen [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) verwenden, um einen [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly) als Textzeichenfolge zu beschreiben. Die Sprache definiert auch Zeichenfolgenelemente zum Beschreiben von Informationen in den Komponenten eines Sicherheitsdeskriptors.

> [!Note]  
> AcEs (Conditional [*Access Control Entries)*](/windows/desktop/SecGloss/a-gly) haben ein anderes SDDL-Format als andere ACE-Typen. AcEs finden Sie unter [ACE-Zeichenfolgen.](ace-strings.md) Informationen zu bedingten ACEs finden Sie unter [Sicherheitsbeschreibungsdefinitionssprache für bedingte ACEs.](security-descriptor-definition-language-for-conditional-aces-.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Security Descriptor String Format](security-descriptor-string-format.md)
</dt> <dt>

[Sicherheitsbeschreibungsdefinitionssprache für bedingte ACEs](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[ACE-Zeichenfolgen](ace-strings.md)
</dt> <dt>

[SID-Zeichenfolgen](sid-strings.md)
</dt> <dt>

[\[MS-DTYP: \] Beschreibungssprache des Sicherheitsdeskriptors](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

 

 
