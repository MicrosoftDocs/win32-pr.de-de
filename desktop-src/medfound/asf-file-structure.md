---
description: In diesem Thema wird die Struktur einer ASF-Datei (Advanced Systems Format) beschrieben.
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: Struktur der ASF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524672"
---
# <a name="asf-file-structure"></a>Struktur der ASF-Datei

In diesem Thema wird die Struktur einer ASF-Datei (Advanced Systems Format) beschrieben.

Ausführliche Informationen zu ASF-Dateien finden Sie in der [ASF-Spezifikation](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea). Sie können auch das [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) -Tool verwenden, um die Struktur einer vorhandenen ASF-Datei anzuzeigen.

Die Basiseinheit der Organisation für ASF-Dateien wird als *Objekt* bezeichnet. Ein Objekt vom Typ "ASF File" enthält die folgenden Daten.



| Daten                                                        | Size     |
|-------------------------------------------------------------|----------|
| Eine GUID, die das Objekt identifiziert.                          | 128 Bits |
| Die Größe des Objekts.                                     | 64 Bits. |
| Objektdaten. Die Objektdaten können andere ASF-Objekte enthalten. | Verschiedene Ursachen.  |



 

> [!Note]  
> Ein ASF-Datei Objekt ist einfach ein Datenblock. Es handelt sich nicht um ein Objekt im Computer Programmier Sinn.

 

Eine ASF-Datei enthält drei Typen von Datei Objekten der obersten Ebene.



| ASF-Datei Objekt                                                                                                                      | BESCHREIBUNG                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Header Objekt<br/>         | Enthält Informationen zur ASF-Datei.<br/>  |
| <span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Datenobjekt<br/>                     | Enthält Pakete von Mediendaten.<br/>           |
| <span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Index Objekt (e)<br/> | Enthält mindestens einen Index. (Optional.)<br/> |



 

Das folgende Diagramm zeigt die Struktur der ASF-Datei.

![Diagramm, das die Struktur der ASF-Datei, einschließlich der Elemente innerhalb des Headers, der Daten und des Indexes, anzeigt](images/asf-components04.png)

Dieses Diagramm wird nicht zum Skalieren gezeichnet. in der Regel besteht das Datenobjekt aus dem größten Teil der Datei.

### <a name="header-object"></a>Header Objekt

Das Header Objekt ist obligatorisch und wird am Anfang jeder ASF-Datei angezeigt. Sie enthält globale Dateiattribute und Informationen zu den Datenströmen in der ASF-Datei. Diese Informationen werden verwendet, um die Daten in der Datei zu interpretieren und wiederzugeben.

Das Header Objekt enthält mehrere madatory-unter Objekte:

-   Das Dateieigenschaften Objekt beschreibt globale Attribute der Datei, z. b. die Dateigröße, die Wiedergabedauer, die Anzahl von Datenpaketen, die minimale und die maximale Paketgröße und die maximale Bitrate.
-   Das Header Erweiterungs Objekt ermöglicht das Hinzufügen zusätzlicher Funktionen zu einer ASF-Datei, während die Abwärtskompatibilität beibehalten wird.
-   Das Stream Properties-Objekt beschreibt einen Stream in der Datei. Eine ASF-Datei muss mindestens einen Stream und somit mindestens ein Stream Properties-Objekt enthalten.

Das Header Objekt kann zusätzliche optionale Informationen enthalten, einschließlich Metadaten über die Datei (z. b. Titel und Autor), eine Liste der Codecs, die zum Codieren der Datei verwendet werden, sowie Informationen zum Inhalts Schutz.

### <a name="data-object"></a>Datenobjekt

Das ASF-Datenobjekt enthält alle Mediendaten für die ASF-Datei. Dieses Objekt ist obligatorisch und muss dem ASF-Header Objekt folgen.

Das Datenobjekt wird in Daten *Pakete* aufgeteilt. Jedes Paket enthält Daten für einen oder mehrere Datenströme in der Datei. Ein Datenpaket enthält einen datenpaketheader, der Informationen zur Paketverarbeitung bereitstellt, gefolgt von den Nutzlastdaten der tatsächlichen digitalen Mediendaten. Allen Datenpaketen ist eine Präsentationszeit zugeordnet, die in der empfangenen Reihenfolge angeordnet ist.

Informationen zum Inhalt des Datenobjekts, z. b. Paketgröße und Paket Anzahl, werden im Header Objekt gespeichert.

### <a name="index-object"></a>Index-Objekt

Das Index Objekt ist optional und ist das letzte Objekt in der ASF-Datei. Eine ASF-Datei kann mehr als ein Index Objekt enthalten. Das Index-Objekt bietet zeitbasierten zufälligen Zugriff auf das ASF-Datenobjekt.

Ein einfaches Index Objekt ist ein anderer Indextyp.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




