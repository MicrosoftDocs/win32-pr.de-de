---
title: Software-Shader
description: Software-Shader werden implementiert, um die Entwicklung von Shadern ohne zugrunde liegende Hardwareunterstützung zu ermöglichen. Sie unterstützen den vollständigen Featuresatz. Da Sie in Software implementiert werden, erzielen Sie nicht die beste Leistung.
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df101edd0362321847fb9c0baf7feb3cc865e2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037634"
---
# <a name="software-shaders"></a>Software-Shader

Software-Shader werden implementiert, um die Entwicklung von Shadern ohne zugrunde liegende Hardwareunterstützung zu ermöglichen. Sie unterstützen den vollständigen Featuresatz. Da Sie in Software implementiert werden, erzielen Sie nicht die beste Leistung.



| Version   | Funktionsgruppe                  | Requirements (Anforderungen)                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| vs \_ 2 \_ SW | Alle Features von vs \_ 2 \_ x | Wird nur von der Verarbeitung von Software Scheitel Punkten und einem Referenzgerät unterstützt. |
| vs \_ 3- \_ SW | Alle Features von vs \_ 3 \_ 0 | Wird nur von der Verarbeitung von Software Scheitel Punkten und einem Referenzgerät unterstützt. |
| PS \_ 2 \_ SW | Alle Features von PS \_ 2 \_ x | Wird nur von einem Referenzgerät unterstützt.                                |
| PS \_ 3 ( \_ SW) | Alle Features von PS \_ 3 \_ 0 | Wird nur von einem Referenzgerät unterstützt.                                |



 

Einige Überprüfungen werden für Software-Shader gelockert. Dies ist nützlich für das Debuggen und das Prototypen. Die folgenden Überprüfungen werden gelockert: (alle anderen Überprüfungen bleiben unverändert)



| Überprüfungstyp                                 | Suchende                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anweisungs Anzahl:                             | Dies wird für vs \_ 2 \_ SW, vs \_ 3 \_ SW und PS \_ 2 \_ SW, PS \_ 3 SW, gelockert \_ . Es sind unbegrenzte Anweisungen zulässig.                                                                                                              |
| Konstante Anzahl von Gleit Komma Werten:                          | Dies wird für vs \_ 2 \_ SW, vs \_ 3 \_ SW und PS \_ 2 \_ SW, PS \_ 3 SW, gelockert \_ . Bis zu 8192 Konstanten sind zulässig.                                                                                                                |
| Ganzzahlige Konstante Anzahl:                        | Dies wird für vs \_ 2 \_ SW, vs \_ 3 \_ SW und PS \_ 2 \_ SW, PS \_ 3 SW, gelockert \_ . Bis zu 2048 Konstanten sind zulässig.                                                                                                                |
| Anzahl von booleschen Konstanten:                        | Dies wird für vs \_ 2 \_ SW, vs \_ 3 \_ SW und PS \_ 2 \_ SW, PS \_ 3 SW, gelockert \_ . Bis zu 2048 Konstanten sind zulässig.                                                                                                                |
| Abhängige Lese Tiefe:                           | Dies wird für PS \_ 2 \_ SW gelockert. Wie in vs \_ 3 \_ 0 und PS \_ 3 \_ 0 sind unbegrenzte abhängige Lesevorgänge zulässig.                                                                                                                |
| Anzahl der Anweisungen und Bezeichnungen der Fluss Steuerung: | Dies wird für vs \_ 2 \_ SW gelockert. Es sind unbegrenzte Anweisungen zur Fluss Steuerung und bis zu 2048 Bezeichnungen zulässig.                                                                                                                |
| Schleifen Anzahl/Start/Schritt:                          | Diese werden für vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW und PS \_ 3 SW gelockert \_ . Die Schrittgröße der Iterations-und Interpunktions Schritte für rep-und Loop-Anweisungen sind 32-Bit-interkte mit Vorzeichen. Die Anzahl der interationen kann maximal \_ int/64 betragen. |
| Grenzwerte für den Lesezugriff:                               | vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW und PS \_ 3 \_ SW haben keinen Grenzwert für Lesevorgänge.                                                                                                                                              |
| Anzahl der Interpolatoren:                        | Es gibt 16 [Register-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) in vs \_ 3 \_ SW und 10 [PS \_ 3 \_ 0 Registern](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# ) für PS \_ 3 \_ SW.     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASM-Shader-Referenz](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




