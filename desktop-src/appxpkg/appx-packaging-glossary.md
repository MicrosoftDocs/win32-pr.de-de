---
title: Glossar für Verpacken, Bereitstellung und Abfrage
description: Enthält Definitionen für Begriffe im Zusammenhang mit der Paket Erstellung, Bereitstellung und Abfrage von Windows-apps.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a2112b593e2d2a5aaf4f06525160e2d799bad1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104390135"
---
# <a name="packaging-deployment-and-query-glossary"></a>Glossar für Verpacken, Bereitstellung und Abfrage

<dl> <dt>

<span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**ID des Anwendungs Benutzer Modells**
</dt> <dd>

Mit der App-Benutzer Modell-ID wird eine APP auf dem Betriebssystem eindeutig identifiziert, damit das Betriebssystem Benachrichtigungen an die APP senden kann.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**Zuordnung blockieren**
</dt> <dd>

Definiert die Indizes und kryptografischen Hashes für Blöcke ausführbaren Codes und Daten, die in den Dateien eines App-Pakets gespeichert werden. Für jedes app-Paket ist eine BlockMap.xml-Datei erforderlich.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**Abhängigkeits Paket**
</dt> <dd>

Ein Paket, von dem ein anderes Paket abhängt. Die Abhängigkeit wird im Manifest des abhängigen Pakets deklariert, nicht im Manifest des Abhängigkeits Pakets.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**abhängiges Paket**
</dt> <dd>

Ein Paket, das eine Abhängigkeit von einem anderen Paket annimmt. Die Abhängigkeit wird im Manifest des abhängigen Pakets deklariert.

</dd> <dt>

<span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**Dateien mit Speicherbedarf**
</dt> <dd>

Dateien innerhalb eines App-Pakets, die nicht Teil der APP sind, die bereitgestellt werden soll. Diese Dateien stellen Metadaten für das Paket bereit. Standard Dateien für den Speicherbedarf sind das Manifest, Block Map, Stream Map und digitale Signatur. Die Speicherbedarf-Dateien werden im Rahmen des paketbuildprozesses erstellt. Zusätzlich zu den OPC \[ -Spezifikationen sind Inhalts \_ Typen \] . XML und Dateien, deren Namen dem \* \\ \_ Muster "rels \\ \* . rels" entsprechen, Dateien für den Speicherbedarf.

</dd> <dt>

<span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**kundiger**
</dt> <dd>

Eine XML-Datei, in der die Inhalte und Metadaten beschrieben werden, die einem Paket einschließlich der Paket-ID zugeordnet sind. Für jedes app-Paket ist eine Manifest-XML-Datei erforderlich.

</dd> <dt>

<span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**
</dt> <dd>

In den Open Packaging Conventions (OPC) wird eine Containerdatei Technologie beschrieben, die in den ISO/IEC 29500-und ECMA 376-Standards dokumentiert ist. App-Pakete sind OPC-kompatibel.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**Paketen**
</dt> <dd>

Die Einheit für die Bereitstellung, Verwaltung und Wartung von Software, die dem App-Paket Modell zugeordnet ist. Ein Paket enthält die Dateien, die die APP bilden, sowie eine Manifest-Datei, in der die Software für Windows beschrieben wird.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**Paket Familienname**
</dt> <dd>

Eine serialisierte Form der Paket-ID, die die Paket Familie auf dem Computer eindeutig darstellt. Sie eignet sich für das Benennen von Objekten wie z. b. Dateien und Ordnern. Der Paket Familienname ähnelt dem vollständigen Paketnamen, enthält jedoch nur den Namen und den Verleger. Da Informationen ausgeschlossen werden, die sich durch die Wartung (Version, Architektur und Ressourcen Informationen) ändern, ist es für Versions unabhängige Verweise auf das Paket nützlich.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**vollständiger Paketname**
</dt> <dd>

Eine serialisierte Form der Paket-ID, die diese Version des Pakets auf dem Computer eindeutig darstellt. Sie eignet sich für das Benennen von Objekten wie z. b. Dateien und Ordnern.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**Paket-ID**
</dt> <dd>

Eine Globally Unique Identifier für ein Paket. Sie besteht aus einem Tupel von Attributen für das Paket, einschließlich Name, Herausgeber, unterstützte Architektur, Ressourcen Informationen und Version. Siehe den vollständigen Namen des Pakets und den Paket Familiennamen für serialisierte Formen der Paket-ID.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**Paket relative Anwendungs-ID**
</dt> <dd>

Das **ID** -Attribut für das [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) -Element im Paket Manifest, das auch als "Praid" bezeichnet wird. Mit dieser Zeichenfolge wird eine APP innerhalb eines Pakets eindeutig identifiziert. Dieses Attribut ist für das **Application** -Element erforderlich.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**Nutz Last Dateien**
</dt> <dd>

Die Dateien innerhalb eines App-Pakets, die Teil der APP sind, die bereitgestellt werden soll. Diese Dateien werden extrahiert und im Installationsordner des Benutzers abgelegt.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**Ressourcen-ID**
</dt> <dd>

Ein optionaler Teil einer Paket-ID, der verwendet wird, um die Ressourcen im Paket zu unterscheiden. Beispielsweise kann eine Ressourcen-ID verwendet werden, um die Sprache oder das Gebiets Schema anzugeben.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Zentrales Zip-Verzeichnis**
</dt> <dd>

Die Byte Sequenzen in einer ZIP-Datei, in der Metadaten zum ZIP-Archiv und dessen Inhalt gespeichert werden, einschließlich Name, Größe, Komprimierungs Einstellungen und Speicherort innerhalb des Archivs.

</dd> </dl>

 

 