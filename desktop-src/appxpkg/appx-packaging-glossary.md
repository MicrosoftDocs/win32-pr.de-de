---
title: Paket-, Bereitstellungs- und Abfrageglossar
description: Stellt Definitionen für Begriffe im Zusammenhang mit der Paketierung, Bereitstellung und Abfrage für Windows-Apps bereit.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a273b82806a724e50c7f29c512d19e1723283582abb3aa8b97f49f6293182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130272"
---
# <a name="packaging-deployment-and-query-glossary"></a>Paket-, Bereitstellungs- und Abfrageglossar

<dl> <dt>

<span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**Modell-ID des Anwendungsbenutzers**
</dt> <dd>

Die Id des Anwendungsbenutzermodells identifiziert eine App im Betriebssystem eindeutig, sodass das Betriebssystem Benachrichtigungen senden kann usw. an die App.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**Blockzuordnung**
</dt> <dd>

Definiert die Indizes und kryptografischen Hashes für Blöcke von ausführbarem Code und Daten, die in den Dateien eines App-Pakets gespeichert sind. Für jedes App-Paket ist eine BlockMap.xml-Datei erforderlich.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**Abhängigkeitspaket**
</dt> <dd>

Ein Paket, von dem ein anderes Paket abhängt. Die Abhängigkeit wird im Manifest des abhängigen Pakets und nicht im Manifest des Abhängigkeitspakets deklariert.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**Abhängiges Paket**
</dt> <dd>

Ein Paket, das eine Abhängigkeit von einem anderen Paket annimmt. Die Abhängigkeit wird im Manifest des abhängigen Pakets deklariert.

</dd> <dt>

<span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**Speicherbedarfsdateien**
</dt> <dd>

Dateien in einem App-Paket, die nicht Teil der bereitzustellenden App sind. Diese Dateien stellen Metadaten für das Paket bereit. Standard-Speicherbedarfsdateien umfassen das Manifest, die Blockzuordnung, die Streamzuordnung und die digitale Signatur. Speicherbedarfsdateien werden im Rahmen des Paketerstellungsprozesses erstellt. Zusätzlich zur OPC-Spezifikation \[ \_ sind Inhaltstypen \].xml und Dateien, deren Namen dem \* \\ \_ Muster "rels.rels" \\ \* entsprechen, Speicherbedarfsdateien.

</dd> <dt>

<span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**Manifest**
</dt> <dd>

Eine XML-Datei, die den Inhalt und die Metadaten beschreibt, die einem Paket zugeordnet sind, einschließlich der Paket-ID. Für jedes App-Paket ist eine MANIFEST-XML-Datei erforderlich.

</dd> <dt>

<span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**Opc**
</dt> <dd>

Open Packaging-Konventionen (OPC) beschreibt eine Containerdateitechnologie, die in den ISO/IEC 29500- und ECMA 376-Standards dokumentiert ist. App-Pakete sind OPC-konform.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**Paket**
</dt> <dd>

Die Einheit von Bereitstellungs-, Verwaltungs- und Wartungssoftware, die dem App-Paketmodell zugeordnet ist. Ein Paket enthält die Dateien, aus denen die App besteht, sowie eine Manifestdatei, die die zu Windows software beschreibt.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**Paketfamilienname**
</dt> <dd>

Eine serialisierte Form der Paket-ID, die die Paketfamilie auf dem Computer eindeutig darstellt. Es eignet sich zum Benennen von Objekten wie Dateien und Ordnern. Der Name der Paketfamilie ähnelt dem vollständigen Namen des Pakets, enthält jedoch nur den Namen und den Herausgeber. Da sie Informationen ausschließt, die sich mit der Wartung ändern (Version, Architektur und Ressourceninformationen), ist sie nützlich für versionsunabhängige Verweise auf das Paket.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**vollständiger Paketname**
</dt> <dd>

Eine serialisierte Form der Paket-ID, die diese Version des Pakets auf dem Computer eindeutig darstellt. Es eignet sich zum Benennen von Objekten wie Dateien und Ordnern.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**Paket-ID**
</dt> <dd>

Ein global eindeutiger Bezeichner für ein Paket. Es besteht aus einem Tupel von Attributen für das Paket, einschließlich Name, Herausgeber, unterstützter Architektur, Ressourceninformationen und Version. Informationen zu serialisierten Formularen der Paket-ID finden Sie unter Vollständiger Paketname und Paketfamilienname.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**Relative Anwendungs-ID des Pakets**
</dt> <dd>

Das **Id-Attribut** für das [**Application-Element**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) im Paketmanifest, das auch als PRAID bezeichnet wird. Diese Zeichenfolge identifiziert eine App innerhalb eines Pakets eindeutig. Dieses Attribut ist für das **Application-Element** erforderlich.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**Nutzlastdateien**
</dt> <dd>

Die Dateien in einem App-Paket, die Teil der bereitzustellenden App sind. Diese Dateien werden extrahiert und im Installationsordner des Benutzers abgelegt.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**Ressourcen-ID**
</dt> <dd>

Ein optionaler Teil einer Paket-ID, der verwendet wird, um die Ressourcen im Paket zu unterscheiden. Beispielsweise kann eine Ressourcen-ID verwendet werden, um die Sprache oder das Gebietsschema anzugeben.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Zentrales ZIP-Verzeichnis**
</dt> <dd>

Die Bytesequenzen in einer ZIP-Datei, die Metadaten zum ZIP-Archiv und dessen Inhalt speichern, einschließlich Name, Größe, Komprimierungseinstellungen und Speicherort im Archiv.

</dd> </dl>

 

 