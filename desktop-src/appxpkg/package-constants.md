---
title: Paket Konstanten (appmodel. h)
description: Gibt an, wie Pakete verarbeitet werden sollen.
ms.assetid: 72E565C3-6CFD-47E3-8BAC-17D6E86B99DA
topic_type:
- apiref
api_name:
- PACKAGE_APPLICATIONS_MAX_COUNT
- PACKAGE_APPLICATIONS_MIN_COUNT
- PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES
- PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES
- PACKAGE_FILTER_ALL_LOADED
- PACKAGE_FILTER_BUNDLE
- PACKAGE_FILTER_DIRECT
- PACKAGE_FILTER_HEAD
- PACKAGE_FILTER_OPTIONAL
- PACKAGE_FILTER_RESOURCE
- PACKAGE_GRAPH_MAX_SIZE
- PACKAGE_GRAPH_MIN_SIZE
- PACKAGE_INFORMATION_BASIC
- PACKAGE_INFORMATION_FULL
- PACKAGE_MAX_DEPENDENCIES
- PACKAGE_MIN_DEPENDENCIES
- PACKAGE_PROPERTY_BUNDLE
- PACKAGE_PROPERTY_DEVELOPMENT_MODE
- PACKAGE_PROPERTY_FRAMEWORK
- PACKAGE_PROPERTY_OPTIONAL
- PACKAGE_PROPERTY_RESOURCE
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb3a4630eb6e132c7a82ea6b45839f6d2684cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340317"
---
# <a name="package-constants"></a>Paket Konstanten

Gibt an, wie Pakete verarbeitet werden sollen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_APPLICATIONS_MAX_COUNT"></span><span id="package_applications_max_count"></span><dl> <dt><strong>PACKAGE_APPLICATIONS_MAX_COUNT</strong></dt> <dt>100</dt> </dl></td>
<td style="text-align: left;">Die maximale Anzahl von apps in einem Paket.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_APPLICATIONS_MIN_COUNT"></span><span id="package_applications_min_count"></span><dl> <dt><strong>PACKAGE_APPLICATIONS_MIN_COUNT</strong></dt> <dt>0</dt> </dl></td>
<td style="text-align: left;">Die Mindestanzahl von apps in einem Paket.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES"></span><span id="package_family_max_resource_packages"></span><dl> <dt><strong>PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES</strong></dt> <dt>512</dt> </dl></td>
<td style="text-align: left;">Die maximal zulässige Anzahl von Ressourcen Paketen für ein Paket.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES"></span><span id="package_family_min_resource_packages"></span><dl> <dt><strong>PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES</strong></dt> <dt>0</dt> </dl></td>
<td style="text-align: left;">Die Mindestanzahl von Ressourcen Paketen, die ein Paket enthalten kann.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_ALL_LOADED"></span><span id="package_filter_all_loaded"></span><dl> <dt><strong>PACKAGE_FILTER_ALL_LOADED</strong></dt> <dt>0x00000000</dt> </dl></td>
<td style="text-align: left;">Verarbeiten Sie alle Pakete im Abhängigkeits Diagramm.<br/> Dies entspricht <strong>PACKAGE_FILTER_HEAD</strong>  |  <strong>PACKAGE_FILTER_DIRECT</strong>.<br/>
<blockquote>
[!Note]<br />
<strong>PACKAGE_FILTER_ALL_LOADED</strong> können nach Windows 8.1 geändert werden oder für Releases nicht verfügbar sein. Verwenden Sie stattdessen <strong>PACKAGE_FILTER_HEAD</strong>  |  <strong>PACKAGE_FILTER_DIRECT</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_BUNDLE"></span><span id="package_filter_bundle"></span><dl> <dt><strong>PACKAGE_FILTER_BUNDLE</strong></dt> <dt>0x00000080</dt> </dl></td>
<td style="text-align: left;">Verarbeiten von Paket Paketen im Paket Diagramm.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_DIRECT"></span><span id="package_filter_direct"></span><dl> <dt><strong>PACKAGE_FILTER_DIRECT</strong></dt> <dt>0x00000020</dt> </dl></td>
<td style="text-align: left;">Verarbeiten Sie die direkt abhängigen Pakete des Head (First)-Pakets im Abhängigkeits Diagramm.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_HEAD"></span><span id="package_filter_head"></span><dl> <dt><strong>PACKAGE_FILTER_HEAD</strong></dt> <dt>0x00000010</dt> </dl></td>
<td style="text-align: left;">Verarbeiten Sie das erste Paket im Abhängigkeits Diagramm.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_OPTIONAL"></span><span id="package_filter_optional"></span><dl> <dt><strong>PACKAGE_FILTER_OPTIONAL</strong></dt> <dt>0x00020000</dt> </dl></td>
<td style="text-align: left;">Verarbeiten von Paket Paketen im Paket Diagramm.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_RESOURCE"></span><span id="package_filter_resource"></span><dl> <dt><strong>PACKAGE_FILTER_RESOURCE</strong></dt> <dt>0x00000040</dt> </dl></td>
<td style="text-align: left;">Verarbeiten von Ressourcen Paketen im Paket Diagramm.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_GRAPH_MAX_SIZE"></span><span id="package_graph_max_size"></span><dl> <dt><strong>PACKAGE_GRAPH_MAX_SIZE</strong></dt> <dt>(1 + PACKAGE_MAX_DEPENDENCIES + PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES)</dt> </dl></td>
<td style="text-align: left;">Die maximale Größe eines Paket Diagramms.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_GRAPH_MIN_SIZE"></span><span id="package_graph_min_size"></span><dl> <dt><strong>PACKAGE_GRAPH_MIN_SIZE</strong></dt> <dt>1</dt> </dl></td>
<td style="text-align: left;">Die minimale Größe eines Paket Diagramms.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_INFORMATION_BASIC"></span><span id="package_information_basic"></span><dl> <dt><strong>PACKAGE_INFORMATION_BASIC</strong></dt> <dt>0x00000000</dt> </dl></td>
<td style="text-align: left;">Rufen Sie grundlegende Informationen ab.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_INFORMATION_FULL"></span><span id="package_information_full"></span><dl> <dt><strong>PACKAGE_INFORMATION_FULL</strong></dt> <dt>0x00000100</dt> </dl></td>
<td style="text-align: left;">Abrufen von vollständigen Informationen<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_MAX_DEPENDENCIES"></span><span id="package_max_dependencies"></span><dl> <dt><strong>PACKAGE_MAX_DEPENDENCIES</strong></dt> <dt>128</dt> </dl></td>
<td style="text-align: left;">Die maximale Anzahl von Paketen, von denen ein Paket abhängt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_MIN_DEPENDENCIES"></span><span id="package_min_dependencies"></span><dl> <dt><strong>PACKAGE_MIN_DEPENDENCIES</strong></dt> <dt>0</dt> </dl></td>
<td style="text-align: left;">Die Mindestanzahl von Paketen, von denen ein Paket abhängt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_BUNDLE"></span><span id="package_property_bundle"></span><dl> <dt><strong>PACKAGE_PROPERTY_BUNDLE</strong></dt> <dt>0x00000004</dt> </dl></td>
<td style="text-align: left;">Das Paket ist ein Bündel Paket.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_DEVELOPMENT_MODE"></span><span id="package_property_development_mode"></span><dl> <dt><strong>PACKAGE_PROPERTY_DEVELOPMENT_MODE</strong></dt> <dt>0x00010000 bis</dt> </dl></td>
<td style="text-align: left;">Das Paket wurde mit der <a href="/uwp/api/Windows.Management.Deployment.DeploymentOptions"><strong>deploymentoptions</strong></a> -Enumeration registriert.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_FRAMEWORK"></span><span id="package_property_framework"></span><dl> <dt><strong>PACKAGE_PROPERTY_FRAMEWORK</strong></dt> <dt>0x00000001</dt> </dl></td>
<td style="text-align: left;">Das Paket ist ein Framework.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_OPTIONAL"></span><span id="package_property_optional"></span><dl> <dt><strong>PACKAGE_PROPERTY_OPTIONAL</strong></dt> <dt>0x00000008</dt> </dl></td>
<td style="text-align: left;">Das Paket ist ein optionales Paket.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_RESOURCE"></span><span id="package_property_resource"></span><dl> <dt><strong>PACKAGE_PROPERTY_RESOURCE</strong></dt> <dt>0x00000002</dt> </dl></td>
<td style="text-align: left;">Das Paket ist ein Ressourcenpaket.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Appmodel. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getcurrentpackageingefo**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)
</dt> <dt>

[**Getpackageingefo**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)
</dt> <dt>

[**Packageidfromfullname**](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)
</dt> </dl>

 

