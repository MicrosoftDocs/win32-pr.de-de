---
description: Ein X.509-Zertifikat der Version 3 enthält die Felder, die in Version 1 und Version 2 definiert sind, und es werden Zertifikaterweiterungen hinzugefügt. Die ASN. 1-Syntax von Zertifikat Erweiterungen wird im folgenden Beispiel gezeigt.
ms.assetid: ca8df7a4-caa4-4fe7-81a8-8fce372454f4
title: Erweiterungen der Version 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee23ce35ba7031a1a9f7a2c9caa79fd955ccbe2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215999"
---
# <a name="version-3-extensions"></a>Erweiterungen der Version 3

Ein X.509-Zertifikat der Version 3 enthält die Felder, die in Version 1 und Version 2 definiert sind, und es werden Zertifikaterweiterungen hinzugefügt. Die ASN. 1-Syntax von Zertifikat Erweiterungen wird im folgenden Beispiel gezeigt.

``` syntax
---------------------------------------------------------------------
-- Extensions (beginning with version 3).
---------------------------------------------------------------------
Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
  Id                  OBJECT IDENTIFIER,
  critical            BOOLEAN DEFAULT FALSE,
  extnValue           OCTET STRING
}
```

In der folgenden Tabelle sind die Standard Erweiterungen der Version 3 und ihre Objekt-IDs (OIDs) aufgeführt. Microsoft unterstützt diese und umfasst zusätzliche benutzerdefinierte Erweiterungen. Weitere Informationen finden Sie unter [Erweiterungen](extensions.md).

| Durchwahl                                         | BESCHREIBUNG                                                                                                                                                                                              |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Autoritäts Bezeichner der Zertifizierungsstelle (2.5.29.19)<br/>    | Gibt den öffentlichen Schlüssel der Zertifizierungsstelle an, der dem privaten Schlüssel der Zertifizierungsstelle entspricht, mit dem das Zertifikat signiert wird.                                                                              |
| Grundlegende Einschränkungen (2.5.29.35)<br/>           | Gibt an, ob die Entität als Zertifizierungsstelle fungieren kann, und wenn dies der Fall ist, wie viele untergeordnete Zertifizierungsstellen in der Zertifikatkette darunter vorhanden sein können.                                                           |
| Zertifikat Richtlinien (2.5.29.32)<br/>        | Gibt die Richtlinien an, unter denen das Zertifikat ausgestellt wurde, sowie die Zwecke, für die es genutzt werden kann.                                                                                            |
| CRL-Verteilungs Punkte (2.5.29.31)<br/>     | Enthält den URI der Basis [*Zertifikat Sperr Liste*](/windows/desktop/SecGloss/c-gly) (CRL).                                  |
| Erweiterte Schlüssel Verwendung (2.5.29.46)<br/>          | Gibt die Art und Weise an, in welcher der öffentliche Schlüssel im Zertifikat verwendet werden kann.                                                                                                                   |
| Alternativer Aussteller Name (2.5.29.8)<br/>      | Gibt einen oder mehrere alternative Namen für den Aussteller der Zertifikatanforderung an.                                                                                                                  |
| Schlüssel Verwendung (2.5.29.15)<br/>                   | Gibt die Einschränkungen für die Vorgänge an, die durch den öffentlichen Schlüssel im Zertifikat ausgeführt werden können.                                                                                           |
| Namens Einschränkungen (2.5.29.30)<br/>            | Gibt den Namespace an, in dem alle Antragstellernamen in einer Zertifikathierarchie liegen müssen. Die Erweiterung wird lediglich in einem Zertifizierungsstellenzertifikat verwendet.                                                       |
| Richtlinien Einschränkungen (2.5.29.36)<br/>          | Schränkt die Zertifikatüberprüfung ein, indem die Richtlinienzuordnung untersagt oder gefordert wird, dass jedes Zertifikat in der Hierarchie eine akzeptable Richtlinienkennung aufweisen muss. Die Erweiterung wird lediglich in einem Zertifizierungsstellenzertifikat verwendet. |
| Richtlinien Zuordnungen (2.5.29.33)<br/>             | Gibt die Richtlinien in einer untergeordneten Zertifizierungsstelle an, die Richtlinien in der ausstellenden Zertifizierungsstelle entsprechen.                                                                                                                |
| Verwendungs Zeitraum für privaten Schlüssel (2.5.29.16)<br/>    | Gibt einen anderen Gültigkeitszeitraum für den privaten Schlüssel als für das Zertifikat an, dem der private Schlüssel zugeordnet ist.                                                                             |
| Alternativer Antragsteller Name (2.5.29.17)<br/>    | Gibt einen oder mehrere alternative Namen für den Antragsteller der Zertifikatanforderung an. Beispiele für alternative Namen sind E-Mail-Adressen, DNS-Namen, IP-Adressen und URIs.                           |
| Attribute des betreffverzeichnisses (2.5.29.9)<br/> | Vermittelt identifizierende Attribute, beispielsweise die Nationalität des Zertifikatantragstellers. Der Erweiterungswert ist eine Folge von OID-Wertepaaren.                                                              |
| Subjekt Schlüssel Bezeichner (2.5.29.14)<br/>      | Unterscheidet zwischen mehreren öffentlichen Schlüsseln im Besitz des Zertifikatantragstellers. Der Erweiterungswert ist normalerweise ein SHA-1-Hash des Schlüssels.                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Felder](about-basic-fields.md)
</dt> <dt>

[Felder der Version 2](about-version-2-fields.md)
</dt> <dt>

[X. 509-Zertifikate für öffentliche Schlüssel](about-x-509-public-key-certificates.md)
</dt> </dl>

 

