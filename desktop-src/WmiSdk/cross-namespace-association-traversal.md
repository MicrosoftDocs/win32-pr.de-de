---
description: Ab Windows 7 implementierte Windows-Verwaltungsinstrumentation (WMI) einen Standardmechanismus zum Ermitteln von Profilen mithilfe des CIM-Schemas.
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: Cross-Namespace Association Traversal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864028"
---
# <a name="cross-namespace-association-traversal"></a>Cross-Namespace Association Traversal

Ab Windows 7 implementierte Windows-Verwaltungsinstrumentation (WMI) einen Standardmechanismus zum Ermitteln von Profilen mithilfe des CIM-Schemas.

WMI unterstützt die Registrierung von Cross-Namespace Association und Association Profile. Weitere Informationen zur Profil Registrierung und zur CIM-Standard Implementierung von Association Traversal finden Sie unter DSP1033 ( [https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf) )

Zur Unterstützung dieses Features hat die WMI-Infrastruktur die folgenden Schritte durchgeführt:

-   Der Interop-Namespace wurde erstellt: \\ root \\ Interop.
-   Zulässiger Überlaufender Zuordnungs Durchlauf. Zuordnungen, die Namespaces überschreiten, unterstützen das Filtern auf Zuordnungs Klassenebene und auf der implementierten Namespace Ebene.
-   Die Klassen " [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))", " [**CIM \_ ElementConfiguration**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)" und " [**CIM \_ referencedprofile**](cim-referencedprofile.md) " wurden hinzugefügt.
-   Die CIM-Schema Version 2.17.1 Kompatibilität wurde implementiert. Weitere Informationen finden Sie unter [CIM-Schema Kompatibilität](cim-schema-compatibility.md).

## <a name="interop-namespace"></a>Interop-Namespace

Der Interop-Namespace stellt einen allgemeinen Speicherort für eine Client Anwendung bereit, um alle Profile zu ermitteln, die auf einem Computer unterstützt werden. Profile können verwendet werden, um verschiedene Aspekte eines Betriebssystems, eines Speicherarrays oder einer Datenbank zu verwalten.

Alle Interop-Klassen und-Objekte müssen im Namespace "root Interop" definiert werden \\ .

## <a name="cim-classes"></a>CIM-Klassen

Die CIM-Klassen, die in der folgenden Liste beschrieben werden, unterstützen die übergreifende Zuordnung der Namespace Zuordnung.

<dl> <dt>

<span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**CIM- \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))
</dt> <dd>

Wird verwendet, um die Profil Spezifikation zu identifizieren, die als implementiert angekündigt wird. Diese Klasse gibt Informationen an, die den Profilnamen, die Organisation und die Version enthalten, mit denen die Implementierung kompatibel ist.

</dd> <dt>

<span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**CIM \_ elementreformstoprofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dd>

Wird verwendet, um Instanzen von Verwaltungs Elementen, die in Profilen definiert sind, mit der [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) -Klasse zuzuordnen, die die spezifischen Profil Spezifikationen identifiziert, die implementiert werden.

</dd> <dt>

<span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**CIM \_ referencedprofile**](cim-referencedprofile.md)
</dt> <dd>

Wird verwendet, um die Beziehung zwischen Profilen darzustellen.

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a>Implementieren von Cross-Namespace Association Traversal

Der WMI-Dienst ermöglicht die übergreifende Zuordnung von Namespace Zuordnungen. WMI stellt den Interop-Namespace zum Registrieren von Profilen bereit und ordnet diese Profile zu, die in verschiedenen Namespaces implementiert werden. Um jedoch den Zuordnungs Durchlauf zu verwenden, müssen Implementierer die profilklassen sowohl im Interop als auch im implementierten Namespace instanziieren. Weitere Informationen finden Sie unter [Schreiben eines Zuordnungs Anbieters für Interop](writing-an-association-provider-for-interop.md).

Zuordnungen, die Namespaces innerhalb derselben Verwaltungs Umgebung überschreiten, müssen sowohl in der Interop als auch in den implementierten Namespaces instanziiert werden. Andernfalls funktioniert der Zuordnungs Durchlauf nicht. Beispielsweise muss der Anbieter der Energieprofil Zuordnung sowohl mit root/Interop-als auch mit root/cimv2/Power-Namespaces registriert werden. Der Zuordnungs Durchlauf sollte in der Lage sein, von einem der beiden Namespaces zurück zum anderen zu werden. Beispiele für Zuordnungs quersal finden Sie unter [zugreifen auf Daten im Interop-Namespace](accessing-data-in-the-interop-namespace.md).

* * Windows Vista: * *

Wenn nach dem Upgrade auf Windows 7 Interop-Geräteprofile vorhanden sind, die zuvor im Root/Interop-Namespace installiert waren, werden keine Windows 7-profile installiert. Diese Profil Objekte von Drittanbietern überschreiben das Interop-Schema von Windows 7, um die Funktionalität aufrechtzuerhalten. Außerdem wird die Ereignis-ID 5631 für die WMI-Anwendung aufgezeichnet.

Um die Windows 7-Interop-Profile zu erhalten, müssen die Windows 7-Version der Datei "Interop. mof" und die zugehörigen MFL-Dateien kompiliert werden. Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CIM- \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**CIM \_ elementreformstoprofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**CIM \_ referencedprofile**](cim-referencedprofile.md)
</dt> <dt>

[CIM-Schema Kompatibilität](cim-schema-compatibility.md)
</dt> <dt>

[Schreiben eines Zuordnungs Anbieters für Interop](writing-an-association-provider-for-interop.md)
</dt> <dt>

[Zugreifen auf Daten im Interop-Namespace](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
