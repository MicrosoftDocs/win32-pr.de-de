---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 231 bis 240.
ms.assetid: edb3dabb-6a65-4285-97d3-f7025d3bb5da
ms.tgt_platform: multiple
title: Fehler 231 bis 240
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d053cac57eec9d0055dec56bbfab8304ad3f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217961"
---
# <a name="errors-231-through-240"></a>Fehler 231 bis 240

Beschreibt die WMI-SNMP-Anbieter Fehler 231 bis 240.

[Schwerwiegender Fehler 232](#fatal-error-232)

[Schwerwiegender Fehler 233](#fatal-error-233)

[Schwerwiegender Fehler 234](#fatal-error-234)

[Schwerwiegender Fehler 236](#fatal-error-236)

## <a name="fatal-error-232"></a>Schwerwiegender Fehler 232

<dl> <dt>

<span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232, schwerwiegender>: " <fileName> : <Zeile \#>: Aufruf von SNMPv1 SMI-Objekttyp nicht zulässig"**
</dt> <dd>

Modul Syntax Fehler. Sie haben den SNMPv1-spezifischen **Objekttyp** Aufruf in der MIB verwendet, haben jedoch den **/v2c** -Schalter angegeben, der eine strikte Übereinstimmung mit SNMPv2C-Syntax erfordert.

</dd> </dl>

## <a name="fatal-error-233"></a>Schwerwiegender Fehler 233

<dl> <dt>

<span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233, schwerwiegender>: " <fileName> : <line \#>: Aufruf von SNMPv1 SMI Trap-Type unzulässig"**
</dt> <dd>

Modul Syntax Fehler. Sie haben den SNMPv1-spezifischen **Trap-Type-** Aufruf im MIB verwendet, haben jedoch den **/v2c** -Schalter angegeben, der strikte Übereinstimmung mit SNMPv2C-Syntax erfordert.

</dd> </dl>

## <a name="fatal-error-234"></a>Schwerwiegender Fehler 234

<dl> <dt>

<span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234, schwerwiegender>: " <fileName> : <line \#>: der Modul-Identitäts Aufruf ist nur unmittelbar nach dem Import Abschnitt zulässig."**
</dt> <dd>

Modul Syntax Fehler. Der Aufruf der **Modul Identität** ist falsch.

</dd> </dl>

## <a name="fatal-error-236"></a>Schwerwiegender Fehler 236

<dl> <dt>

<span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236, schwerwiegender>: " <fileName> : <line \#>: die Zahl passt nicht in die vom Compiler verwendete 32 Bit-Darstellung."**
</dt> <dd>

Modul Syntax Fehler in Wert Zuweisung. Es gibt einen MIB-Wert Zuweisungs Fehler, bei dem ein ganzzahliger Wert so groß ist, dass er mehr als 32 Bits zur Darstellung benötigt.

</dd> </dl>

 

 



