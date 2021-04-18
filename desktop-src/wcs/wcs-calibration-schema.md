---
title: WCS-Kalibrierungsschema
description: In diesem Thema wird das WCS-Kalibrierungs Schema beschrieben, das das WCS Color Device Model Profile erweitert.
ms.assetid: 99f3e9e3-15b7-4bca-87cc-a3bf3b6d0112
keywords:
- Windows Color System (WCS), Kalibrierung
- WCS (Windows Color System), Kalibrierung
- Bild Farbverwaltung, Kalibrierung
- Farbverwaltung, Kalibrierung
- Farben, Kalibrierung
- Schemas, Kalibrierung
- WCS-Kalibrierung
- Energie
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e859ab9d2b47355db063961004f17a8cc1537694
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106354884"
---
# <a name="wcs-calibration-schema"></a>WCS-Kalibrierungsschema

In diesem Thema wird das WCS-Kalibrierungs Schema beschrieben, das das [WCS Color Device Model Profile](wcs-color-device-model-profile-schema-and-algorithms.md)erweitert.

## <a name="the-wcs-calibration-schema"></a>Das WCS-Kalibrierungs Schema

Die folgende Schema Definition wird verwendet, um die neuen Windows 7-Definitionen anzugeben, die die [WCS Color Device Model Profile](wcs-color-device-model-profile-schema-and-algorithms.md) -Kalibrierung unterstützen.


```C++
<?xml version="1.0" encoding="UTF-8"?>
<!--
  Copyright (C) Microsoft. All rights reserved. The Windows Color System
  color profile schemas may be used according to the terms of the license agreement
  available at https://www.microsoft.com/whdc/device/display/color/wcs_license.mspx.
  -->
<xs:schema
  xmlns:cal="http://schemas.microsoft.com/windows/2007/11/color/Calibration"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2007/11/color/Calibration"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model Calibration profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="AdapterGammaConfiguration">
    <xs:choice>
      <xs:element name="ParameterizedCurves" type="wcs:ParameterizedCurvesType"/>
      <xs:element name="HDRToneResponseCurves" type="wcs:HDRToneResponseCurvesType"/>
    </xs:choice>
  </xs:complexType>

  <xs:complexType name="Calibration">
    <xs:sequence>
      <xs:element name="AdapterGammaConfiguration" type="cal:AdapterGammaConfiguration" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>

</xs:schema>
```



Aus Kompatibilitätsgründen mit Windows Vista sollten Profile, die Kalibrierungs Tags enthalten, das-Attribut enthalten `mc:Ignoreable="cdm_calibration"` .

 

 




