---
title: Farbraum-Typbezeichner
description: Diese Konstanten geben den Typ eines Zeichen Arrays für die Zeichenfolge 2 an. Bei den folgenden Werten handelt es sich um gültige Farb Raum Array Typen.
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 973db6c56dda5bde8614dffa13f461761934fcde
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "106351183"
---
# <a name="color-space-type-identifiers"></a>Farbraum-Typbezeichner

Diese Konstanten geben den Typ eines Zeichen Arrays für die Zeichenfolge 2 an. Bei den folgenden Werten handelt es sich um gültige Farb Raum Array Typen.

<dl> <dt>

<span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**
</dt> <dd> <dl> <dt>



Ein ciebaseda-Farb Raum Array aus dem monochrome Profil erhalten.


</dt> </dl> </dd> <dt>

<span id="CSA_GRAY"></span><span id="csa_gray"></span>**CSA \_ grau**
</dt> <dd> <dl> <dt>



Ein ciebaseda-Farb Raum Array aus dem monochrome Profil erhalten.


</dt> </dl> </dd> <dt>

<span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA \_ ABC**
</dt> <dd> <dl> <dt>



Ein ciebasedabc-Farbraum-Array aus dem RGB-oder L- <sup>\*</sup> a- <sup>\*</sup> b-Profil erhalten.


</dt> </dl> </dd> <dt>

<span id="CSA_DEF"></span><span id="csa_def"></span>**CSA \_ DEF**
</dt> <dd> <dl> <dt>



Ein ciebaseddef-Farbraum-Array aus dem RGB-oder L- <sup>\*</sup> a- <sup>\*</sup> b-Profil erhalten.


</dt> </dl> </dd> <dt>

<span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA \_ RGB**
</dt> <dd> <dl> <dt>



Holen Sie sich ein ciebaseddef-Farbraum, gefolgt von einem ciebasedabc-Farbraum-Array aus dem RGB-Profil. Bei der Ausführung verwendet die Funktion die ciebasedabc-Definition, wenn der Drucker keine ciebaseddef-Farbraum unterstützt.


</dt> </dl> </dd> <dt>

<span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA- \_ Labor**
</dt> <dd> <dl> <dt>



Ruft ein ciebasedabc-Farbraum-Array aus dem L <sup>\*</sup> a <sup>\*</sup> b-Profil ab.


</dt> </dl> </dd> <dt>

<span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA- \_ DEFG**
</dt> <dd> <dl> <dt>



Ein ciebaseddefg-Farbraum-Array aus dem CMYK-Profil wird abgerufen.


</dt> </dl> </dd> <dt>

<span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA \_ CMYK**
</dt> <dd> <dl> <dt>



Ein ciebasedcmyk-Farbraum aus dem CMYK-Profil erhalten.


</dt> </dl> </dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konzepte der grundlegenden Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[ICM-Konstanten](wcs-constants.md)
</dt> </dl>

 

 




