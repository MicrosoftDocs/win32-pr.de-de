---
title: 'WCS-Farbgerätemodell: Profilschema und Algorithmen'
description: Dieses Thema enthält Informationen zum WCS Color Device Model Profile Schema und den zugehörigen Algorithmen. Dieses Thema enthält die folgenden Abschnitte OverviewColor Device Model Profile ArchitectureDas CDMP SchemaWCS CDMP v2.0 Calibration AdditionThe CDMP Schema ElementsColorDeviceModelProfileColorDeviceModelNamespaceVersionVersionDocumentationCRTDevice elementLCDDevice elementProjectorDevice elementScannerDevice elementCameraDevice elementRGBPrinterDevice elementCPRINTPrinterDevice elementRGBVirtualDevice elementPlugInDeviceTypeRGBVirtualMeasurementTypeGammaTypeGammaOffsetGainTypeGammaOffsetGainLinearGainTypeToneResponseCurvesTypeGamutBoundarySamplesTypeFloatPairListCMYKPrinterMeasurementTypeRGBPrinterMeasurementTypeRGBCaptureMeasurementTypeOneBasedIndexRGBProjectorMeasurementTypeDisplayMeasurementTypeMeasurementConditionsTypeGeometryTypeRGBPrimariesGroupNonNegativeCMYKSampleTypeNonNegativeRGBSampleTypeNonNegativeCMYKTypeNonNegativeRGBTypeExtensionTypeNonNegativeXYZTypeXYZTypeThe  CDMP-BaselinealgorithmenCRT-GerätemodellbaselineLCD-GerätemodellbaselineRGB-DruckergerätemodellbaselineRGB Baseline des virtuellen GerätemodellsCLP-DruckergerätemodellbaselineRGB-ProjektorgerätemodellbaselineICC-GerätemodellbaselineRelated-Themen
ms.assetid: bbb3b50d-75fc-476d-a011-af7dcc2ac520
keywords:
- Windows Farbsystem (WCS), Farbgerätemodellprofil (CDMP)
- WCS (Windows Color System), Color Device Model Profile (CDMP)
- Bildfarbverwaltung, Farbgerätemodellprofil (CDMP)
- Farbverwaltung, Farbgerätemodellprofil (CDMP)
- Farben,Farbgerätemodellprofil (CDMP)
- Windows Farbsystem (WCS), Profile
- WCS (Windows Color System), Profiles
- Bildfarbverwaltung,Profile
- Farbverwaltung,Profile
- Farben,Profile
- Schemas,Farbgerätemodellprofil (CDMP)
- Algorithmen,Farbgerätemodellprofil (CDMP)
- Farbgerätemodellprofil (CDMP)
- CDMP (Farbgerätemodellprofil)
- WCS-Farbgerätemodellprofil
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5210da85cd320a80e6b29a59e3cb5ff37c86fd174934832404e4b52cf53bd110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118037901"
---
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a>WCS-Farbgerätemodell: Profilschema und Algorithmen

Dieses Thema enthält Informationen zum WCS Color Device Model Profile-Schema und den zugehörigen Algorithmen.

Dieses Thema enthält folgende Abschnitte:

-   [Übersicht](#overview)
-   [Architektur des Farbgerätemodellprofils](#color-device-model-profile-architecture)
-   [Das CDMP-Schema](#the-cdmp-schema)
-   [WCS CDMP v2.0 Calibration Addition](#wcs-cdmp-v20-calibration-addition)
-   [Die CDMP-Schemaelemente](#the-cdmp-schema-elements)
    -   [ColorDeviceModelProfile](#colordevicemodelprofile)
    -   [ColorDeviceModel](#colordevicemodelprofile)
    -   [NamespaceVersion](#namespaceversion)
    -   [Version](#namespaceversion)
    -   [Dokumentation](#documentation)
    -   [CRTDevice-Element](#crtdevice-element)
    -   [ELEMENT "SOLLDevice"](#lcddevice-element)
    -   [ProjektorDevice-Element](#projectordevice-element)
    -   [ScannerDevice-Element](#scannerdevice-element)
    -   [CameraDevice-Element](#cameradevice-element)
    -   [RGBPrinterDevice-Element](#rgbprinterdevice-element)
    -   [CLIDPrinterDevice-Element](#cmykprinterdevice-element)
    -   [RGBVirtualDevice-Element](#rgbvirtualdevice-element)
    -   [PlugInDeviceType](#plugindevicetype)
    -   [RGBVirtualMeasurementType](#rgbvirtualmeasurementtype)
    -   [GammaType](#gammatype)
    -   [GammaOffsetGainType](#gammaoffsetgaintype)
    -   [GammaOffsetGainLinearGainType](#gammaoffsetgainlineargaintype)
    -   [ToneResponseCurvesType](#toneresponsecurvestype)
    -   [GamutBoundarySamplesType](#gamutboundarysamplestype)
    -   [FloatPairList](#floatpairlist)
    -   [C ENUMERATIONPrinterMeasurementType](#cmykprintermeasurementtype)
    -   [RGBPrinterMeasurementType](#rgbprintermeasurementtype)
    -   [RGBCaptureMeasurementType](#rgbcapturemeasurementtype)
    -   [OneBasedIndex](#onebasedindex)
    -   [RGBProjectorMeasurementType](#rgbprojectormeasurementtype)
    -   [DisplayMeasurementType](#displaymeasurementtype)
    -   [MeasurementConditionsType](#measurementconditionstype)
    -   [GeometryType](#geometrytype)
    -   [RGBPrimariesGroup](#rgbprimariesgroup)
    -   [NonNegativeC ENUMERATIONSampleType](#nonnegativecmyksampletype)
    -   [NonNegativeRGBSampleType](#nonnegativergbsampletype)
    -   [NonNegativeC ENUMERATIONType](#nonnegativecmyktype)
    -   [NonNegativeRGBType](#nonnegativergbtype)
    -   [ExtensionType](#extensiontype)
    -   [NonNegativeXYZType](#nonnegativexyztype)
    -   [XYZType](#nonnegativexyztype)
-   [Die CDMP-Baselinealgorithmen](#the-cdmp-baseline-algorithms)
    -   [CRT-Gerätemodellbaseline](#crt-device-model-baseline)
    -   [BASELINE des GERÄTEMODELLS](#lcd-device-model-baseline)
    -   [RGB-Drucker– Gerätemodellbaseline](#rgb-printer-device-model-baseline)
    -   [RGB-Modellbaseline für virtuelle Geräte](#rgb-virtual-device-model-baseline)
    -   [Modellbaseline des CWERT-Druckergeräts](#cmyk-printer-device-model-baseline)
    -   [RGB-Projektor– Gerätemodellbaseline](#rgb-projector-device-model-baseline)
    -   [BASELINE des GERÄTEMODELLS](#icc-device-model-baseline)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Dieses Schema wird verwendet, um den Inhalt eines Farbgerätemodellprofils (CDMP) anzugeben. Die zugehörigen Baselinealgorithmen werden unten beschrieben.

Das DMP-Schema (Basic Device Model Profile) besteht aus den Messdaten für die Stichprobenentnahme.

Die Samplingkomponente des DMP-XML-Schemas bietet Unterstützung für grundlegende Farbmessungsziele und konzentriert sich auf allgemeine Standardziele und Ziele, die für die Baselinegerätemodelle optimiert sind.

Darüber hinaus stellt das Geräteprofil spezifische Informationen zum Zielgerätemodell und eine Richtlinie zur Verfügung, die das Baseline-Fallbackgerätemodell verwenden kann, wenn das Zielmodell nicht verfügbar ist. Die Profilinstanzen können private Erweiterungen mit xml-Standarderweiterungsmechanismen enthalten.

## <a name="color-device-model-profile-architecture"></a>Architektur des Farbgerätemodellprofils

![Diagramm, das die Informationen zeigt, aus denen sich ein Gerätemodellprofil ergibt.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a>Das CDMP-Schema


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="RGBType">
    <xs:attribute name="R" type="xs:float" use="required"/>
    <xs:attribute name="G" type="xs:float" use="required"/>
    <xs:attribute name="B" type="xs:float" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeRGBType">
    <xs:attribute name="R" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="G" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="B" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeCMYKType">
    <xs:attribute name="C" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="M" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="K" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeRGBSampleType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:NonNegativeRGBType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeCMYKSampleType">
    <xs:sequence>
      <xs:element name="CMYK" type="cdm:NonNegativeCMYKType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:group name="RGBPrimariesGroup">
    <xs:sequence>
      <xs:element name="WhitePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="RedPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="GreenPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BluePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BlackPrimary" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
  </xs:group> 
  
  <xs:complexType name="MeasurementConditionsType">
    <xs:annotation>
      <xs:documentation>
      Optional measurement conditions. 
       
      We only support CIEXYZ for measurement color space in this version. 
      If the white point value from the measurement conditions is not available, 
      the default processing will use
        - "D50" for printer and scanners
        - "D65" for camera and displays.          
      </xs:documentation>
    </xs:annotation>
    <xs:sequence>
      <xs:element name="ColorSpace" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="CIEXYZ"/>
          </xs:restriction>
        </xs:simpleType>    
      </xs:element>
      <xs:choice minOccurs="0">
        <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
        <xs:element name="WhitePointName">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="D50"/>
              <xs:enumeration value="D65"/>
              <xs:enumeration value="A"/>
              <xs:enumeration value="F2"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:choice>
      <xs:element name="Geometry" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="0/45"/>
            <xs:enumeration value="0/diffuse"/>
            <xs:enumeration value="diffuse/0"/>
            <xs:enumeration value="direct"/>
          </xs:restriction>
        </xs:simpleType>   
      </xs:element>
      <xs:element name="ApertureSize" type="xs:int" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="DisplayMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="GrayRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="RedRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="GreenRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="BlueRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBProjectorMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:simpleType name="OneBasedIndex">
    <xs:restriction base="xs:int">
      <xs:minInclusive value="1"/>
    </xs:restriction>
  </xs:simpleType>
    
  <xs:complexType name="RGBCaptureMeasurementType">
    <xs:sequence>
      <xs:element name="PrimaryIndex">
        <xs:complexType>
          <xs:all>
            <xs:element name="White" type="cdm:OneBasedIndex"/>
            <xs:element name="Black" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Red" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Green" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Blue" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Cyan" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Magenta" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Yellow" type="cdm:OneBasedIndex" minOccurs="0"/>
          </xs:all>
        </xs:complexType>
      </xs:element>
      <xs:element name="NeutralIndices">
        <xs:simpleType>
          <xs:list itemType="cdm:OneBasedIndex"/>
        </xs:simpleType>
      </xs:element>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:complexType name="CMYKPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeCMYKSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="GammaType">
    <xs:attribute name="value" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="GammaOffsetGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="GammaOffsetGainLinearGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="LinearGain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="cdm:FloatList"/>
      <xs:element name="Output" type="cdm:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="cdm:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="0" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  
  <xs:complexType name="GamutBoundarySamplesType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:RGBType" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="RGBVirtualMeasurementType">
    <xs:sequence>
      <xs:element name="MaxColorantUsed" type="xs:float"/>
      <xs:element name="MinColorantUsed" type="xs:float"/>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:choice>
        <xs:element name="Gamma" type="cdm:GammaType"/>
        <xs:element name="GammaOffsetGain" type="cdm:GammaOffsetGainType"/>
        <xs:element name="GammaOffsetGainLinearGain" type="cdm:GammaOffsetGainLinearGainType"/>
        <xs:element name="HDRToneResponseCurves" type="cdm:HDRToneResponseCurvesType"/>
      </xs:choice>
      <xs:element name="GamutBoundarySamples" type="cdm:GamutBoundarySamplesType" minOccurs="0"/>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="MeasurementConditions" type="cdm:MeasurementConditionsType" minOccurs="0"/>
        <xs:element name="SelfLuminous" type="xs:boolean" />
        <xs:element name="MaxColorant" type="xs:float"/>
        <xs:element name="MinColorant" type="xs:float"/>
        <xs:choice>
          <xs:element name="CRTDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="LCDDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBProjectorDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBProjectorMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="ScannerDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CameraDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CMYKPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:CMYKPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBVirtualDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBVirtualMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
        </xs:choice>
        <xs:element name="PlugInDevice" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>

```



## <a name="wcs-cdmp-v20-calibration-addition"></a>WCS CDMP v2.0 Calibration Addition

Das **ColorDeviceModel-Element** des CDMP-Schemas wurde in Version Windows 7 aktualisiert und enthält nun das neue Kalibrierungselement. Im Folgenden wird die Änderung des CDMP-Schemas veranschaulicht.


```C++
  ...
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        ...
        <xs:element name="PlugInDevice" minOccurs="0">
             ...
        </xs:element>
        <xs:element name="Calibration" type="cal:Calibration" minOccurs="0"/>
        ...
      <xs:sequence>
    ...
    <xs:complexType>
  ...
```



## <a name="the-cdmp-schema-elements"></a>Die CDMP-Schemaelemente

> [!Note]  
> Primäre Beispiele sind Rot, Grün, Blau, Schwarz und Weiß. Eine primäre Rampe ist eine tonale Rampe von der geringsten Leuchtdichte bis zum vollständigen primären Wert. Die maximale Anzahl von Einträgen in einer Tonverlaufsverlauf beträgt 4096.

 

> [!Note]  
> DMPs müssen über Messdaten verfügen.

 

### <a name="colordevicemodelprofile"></a>ColorDeviceModelProfile

Dieses Element ist vom Typ ColorDeviceModel.

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

### <a name="colordevicemodel"></a>ColorDeviceModel

Dieses Element ist eine Sequenz der folgenden Unterelemente.

1.  ProfileName-Zeichenfolge,
2.  optionale Beschreibungszeichenfolge,
3.  optionale Author-Zeichenfolge,
4.  optional MeasurementConditions MeasurementConditionsType,
5.  Self-Luminous boolesch,
6.  MaxColorant float,
7.  MinColorant float,
8.  Auswahl von Elementen
    1.  CRTDevice,
    2.  VICEDevice,
    3.  RGBProjectorDevice,
    4.  ScannerGeräte,
    5.  CameraDevice,
    6.  RGBPrinterDevice,
    7.  CMYKPrinterDevice,
    8.  RGBVirtualDevice,
9.  PlugInDevice,
10. optionaler Extension ExtensionType

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft. Zeichenfolgenunterelemente haben maximal 10.000 Zeichen. Das MaxColorant-Unterelement muss größer oder gleich 0 (null) und größer als das Unterelement MinColorant sein. MinColorant kann negativ sein.

### <a name="namespaceversion"></a>NamespaceVersion

xmlns:cdm=" http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

targetNamespace=" http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

### <a name="version"></a>Version

Version = "1.0" mit Windows Vista.

**Überprüfungsbedingungen:** Jeder Versionswert &gt; 0.1 oder &lt; =2.0 ist gültig, um nicht breaking changes am Format zu unterstützen.

### <a name="documentation"></a>Dokumentation

Gerätemodellprofilschema.

Copyright (C) Microsoft. All rights reserved.

### <a name="crtdevice-element"></a>CRTDevice-Element

Dieses Element ist eine Sequenz von Unterelementen eines MeasurementData DisplayMeasurementType.

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

### <a name="lcddevice-element"></a>ELEMENTSDevice-Element

Dieses Element ist eine Sequenz von Unterelementen eines MeasurementData DisplayMeasurementType.

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

### <a name="projectordevice-element"></a>ProjectorDevice-Element

Dieses Element ist eine Sequenz von Unterelementen eines MeasurementData RGBProjectorMeasurementType.

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

### <a name="scannerdevice-element"></a>ScannerDevice-Element

Dieses Element ist eine Sequenz von Unterelementen eines MeasurementData RGBCaptureMeasurementType

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

### <a name="cameradevice-element"></a>CameraDevice-Element

Dieses Element ist eine Sequenz von Unterelementen eines MeasurementData RGBCaptureMeasurementType

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

### <a name="rgbprinterdevice-element"></a>RGBPrinterDevice-Element

Dieses Element ist eine Sequenz von Unterelementen eines MeasurementData RGBPrinterMeasurementType.

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

### <a name="cmykprinterdevice-element"></a>CMYKPrinterDevice-Element

Dieses Element ist eine Sequenz von Unterelementen eines MeasurementData CMYKPrinterMeasurementType.

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

### <a name="rgbvirtualdevice-element"></a>RGBVirtualDevice-Element

Dieses Element ist eine Sequenz von Unterelementen eines RGBVirtualMeasurementDataType.

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

### <a name="plugindevicetype"></a>PlugInDeviceType

Dieses Element ist eine Sequenz eines GUID GUIDType und aller Untergeordneten Elemente.

**Überprüfungsbedingungen:** Die GUID wird verwendet, um die DM PlugIn Dll-GUID abzugleichen. Es gibt maximal 100.000 benutzerdefinierte Unterelemente.

### <a name="rgbvirtualmeasurementtype"></a>RGBVirtualMeasurementType

Dieses Element ist eine Sequenz, die aus besteht.

1.  GRUPPE RGBPrimariesGroup
2.  Eine Auswahl von
3.  -   Gamma
    -   GammaOffsetGain
    -   GammaOffsetGainLinearGam
    -   ToneResponseCurves-Elemente

4.  optional GamutBoundarySamples GamutBoundarySamplesType
5.  TimeStamp dateTime

**Überprüfungsbedingungen:** Jedes Unterelement dieser Typen verfügt über eigene Validierungsbedingungen.

### <a name="gammatype"></a>GammaType

Dieses Element ist ein komplexer Typ, der aus dem -Attribut besteht.

-   Gamma NonNegativeFloatType

**Überprüfungsbedingungen:** Dies muss anhand von Branchenfeedback ermittelt werden.

### <a name="gammaoffsetgaintype"></a>GammaOffsetGainType

Dieses Element ist ein komplexer Typ, der aus den Attributen besteht.

-   Gamma NonNegativeFloatType
-   Offset NonNegativeFloatType
-   NonNegativeFloatType erhalten

**Überprüfungsbedingungen:** Dies muss anhand von Branchenfeedback ermittelt werden.

### <a name="gammaoffsetgainlineargaintype"></a>GammaOffsetGainLinearGainType

Dieses Element ist ein komplexer Typ, der aus den Attributen besteht.

-   Gamma NonNegativeFloatType
-   Offset NonNegativeFloatType
-   NonNegativeFloatType erhalten
-   LinearGain NonNegativeFloatType
-   TransitionPoint NonNegativeFloatType.

**Überprüfungsbedingungen:** Dies muss anhand von Branchenfeedback ermittelt werden.

### <a name="toneresponsecurvestype"></a>ToneResponseCurvesType

Dieses Element ist eine Sequenz von

1.  RedTRC FloatPairList
2.  GreenTRC FloatPairList
3.  BlueTRC FloatPairList

Das -Element verfügt auch über ein TRCLength-Attribut vom Typ unsignedint.

**Überprüfungsbedingungen:** Dies muss anhand von Branchenfeedback ermittelt werden.

### <a name="gamutboundarysamplestype"></a>GamutBoundarySamplesType

Dieses Element ist eine Sequenz von RGBTypes.

**Überprüfungsbedingungen:** Derzeit sind die maximalen Höchstwerte begrenzt, die basierend auf branchenbezogenem Feedback begrenzt werden sollen.

### <a name="floatpairlist"></a>FloatPairList

Dieses Element ist eine einfache Liste von Gleitkommapaaren.

**Überprüfungsbedingungen:** Dies muss anhand von Branchenfeedback ermittelt werden.

### <a name="cmykprintermeasurementtype"></a>CMYKPrinterMeasurementType

Dieses Element ist ein

1. Sequenz des ColorCube-Elements, das aus einer Sequenz von Sample NonNegativeCMYKSampleType besteht

2. DateTime-Attribut "TimeStamp".

**Überprüfungsbedingungen:** Um anhand von Branchenfeedback bestimmt zu werden.

### <a name="rgbprintermeasurementtype"></a>RGBPrinterMeasurementType

Dieses Element ist ein

1. Sequenz des ColorCube-Elements, das aus einer Sequenz von Sample NonNegativeRGBSampleType besteht

2. TimeStamp dateTime-Attribut.

**Überprüfungsbedingungen:** Um anhand von Branchenfeedback bestimmt zu werden.

### <a name="rgbcapturemeasurementtype"></a>RGBCaptureMeasurementType

Dieses Element ist eine Sequenz von

1.  complexType von PrimaryIndex
2.  1.  White OneBasedIndex
    2.  Optional Black OneBasedIndex
    3.  Optional Red OneBasedIndex
    4.  Optionaler grüner OneBasedIndex
    5.  Optionaler blauer OneBasedIndex
    6.  Optionaler Cyan OneBasedIndex
    7.  Optionaler Magenta OneBasedIndex
    8.  Optionaler gelber OneBasedIndex

3.  NeutralIndices of lines of OneBasedIndex
4.  ColorSamples-Sequenz von Sample NonNegativeRGBSampleType

Das -Element verfügt auch über ein dateTime-Attribut vom Datentyp TimeStamp.

**Überprüfungsbedingungen:** Um anhand von Branchenfeedback bestimmt zu werden.

### <a name="onebasedindex"></a>OneBasedIndex

Dieses Element ist ein einfacher Typ von Einschränkungsbasis ohne Vorzeichen int mit minInclusive value = "1".

**Überprüfungsbedingungen:** Um anhand von Branchenfeedback bestimmt zu werden.

### <a name="rgbprojectormeasurementtype"></a>RGBProjectorMeasurementType

Dieses Element ist eine Sequenz von

1.  RGBPrimariesGroup-Gruppe
2.  ColorSamples-Element, das aus einer Sequenz von Sample NonNegativeRGBSampleType besteht

Das -Element verfügt auch über ein dateTime-Attribut vom Datentyp TimeStamp.

**Überprüfungsbedingungen:** Um anhand von Branchenfeedback bestimmt zu werden.

### <a name="displaymeasurementtype"></a>DisplayMeasurementType

Dieses Element ist eine Sequenz von

1.  Group RGBPrimariesGroup
2.  GrayRamp der Sequenz von Sample NonNegativeRGBType
3.  RedRamp der Sequenz von Sample NonNegativeRGBType
4.  GreenRamp der Sequenz von Sample NonNegativeRGBType
5.  BlueRamp der Sequenz von Sample NonNegativeRGBType

Das DisplayMeasurementType-Element verfügt auch über das dateTime-Attribut TimeStamp.

**Überprüfungsbedingungen:** Um anhand von Branchenfeedback bestimmt zu werden.

### <a name="measurementconditionstype"></a>MeasurementConditionsType

Der MeasurementConditionsType ist eine Sequenz von Unterelementen, die:

1.  ColorSpace restricted string enumeration value of "CIEXYZ" (Eingeschränkter ColorSpace-Zeichenfolgenenumerationswert von "CIEXYZ"
2.  Optionale Auswahl der WhitePoint NonNegativeXYZType- oder WhitePointName-Zeichenfolgenenumeration der Werte D50, D65, A oder F2
3.  Geometry GeometryType
4.  ApertureSize integer in Millimeter

Die Standardwerte sind:

1.  RGB- und C RGB-Drucker:
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  0/45 GeometryType
    4.  10mm ApertureSize
2.  Scanner:
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  0/45 GeometryType
    4.  10mm ApertureSize
3.  Displays and RGB Virtual Device (Anzeigen und virtuelles RGB-Gerät):
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  0/45 GeometryType
    4.  10mm ApertureSize
4.  Kameras:
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  Direct GeometryType
    4.  10mm ApertureSize

**Überprüfungsbedingungen:** Die Validierung jedes Unterelements wird durch Validierungsbedingungen für diese Unterelemente bestimmt. Wenn ein Unterelement fehlt, wird der gerätemodellspezifische Standardwert verwendet.

### <a name="geometrytype"></a>GeometryType

String

Enumerationswerte:

-   "0/45"
-   "0/diffuse"
-   "diffuse/0"
-   "Direkt"

**Überprüfungsbedingungen:** Alle Werte außer den aufgelisteten Zahlenwerten sind ungültig. Diese Informationen ändern nicht das Baselineverarbeitungsverhalten.

### <a name="rgbprimariesgroup"></a>RGBPrimariesGroup

Dieses Element ist eine Sequenz von

1.  WhitePrimary NonNegativeXYZType
2.  RedPrimary NonNegativeXYZType
3.  GreenPrimary NonNegativeXYZType
4.  BluePrimary NonNegativeXYZTYpe
5.  BlackPrimary NonNegativeXYZType

**Überprüfungsbedingungen:** Um anhand von Branchenfeedback bestimmt zu werden.

### <a name="nonnegativecmyksampletype"></a>NonNegativeC ENUMERATIONSampleType

Dieses Element ist eine Sequenz von

1.  C ENUMERATION NonNegativeC ENUMERATIONType
2.  CIEXYZ NonNegativeXYZType

Das Element verfügt auch über eine optionale Tag-Attributzeichenfolge.

**Überprüfungsbedingungen:** Um anhand von Branchenfeedback bestimmt zu werden.

### <a name="nonnegativergbsampletype"></a>NonNegativeRGBSampleType

Dieses Element ist eine Sequenz von

1.  RGB NonNegativeRGBType
2.  CIEXYZ NonNegativeXYZType

Das Element verfügt auch über eine optionale Tag-Attributzeichenfolge.

**Überprüfungsbedingungen:** Um anhand von Branchenfeedback bestimmt zu werden.

### <a name="nonnegativecmyktype"></a>NonNegativeC ENUMERATIONType

Dieses Element, das aus Attributen besteht

1.  C float
2.  M float
3.  Y float
4.  K float

**Überprüfungsbedingungen:** Dies muss anhand von Branchenfeedback ermittelt werden.

### <a name="nonnegativergbtype"></a>NonNegativeRGBType

Dieses Element besteht aus Attributen.

1.  R float
2.  G float
3.  B float

**Überprüfungsbedingungen:** Dies muss anhand von Branchenfeedback ermittelt werden.

### <a name="extensiontype"></a>ExtensionType

Das ExtensionType-Element ist eine Sequenz eines beliebigen Unterelementtyps und wird für proprietäre Informationen von Nicht-Microsoft-Anwendungen verwendet.

**Überprüfungsbedingungen:** Dieses Element ist optional. Es können maximal 1.000 Erweiterungsunterelemente vorhanden sein.

### <a name="nonnegativexyztype"></a>NonNegativeXYZType

Das NonNegativeXYZType-Element besteht aus drei IEEE-Gleitkommaelementen mit einfacher Genauigkeit mit den Namen "X", "Y" und "Z". Diese Werte sind auf die DMP-Profilmessungswerte beschränkt. Diese Messungen können entweder absolute (nicht relative) CIEXYZ 1931 reflektierende Werte oder absolute (nicht relative) CIEXYZ 1931 direkte (transmissive) Werte in Candelas pro Quadrateinheiten pro Meter sein.

**Überprüfungsbedingungen:** Nur reale Werte sind gültig, und negative CIEXYZ-Messwerte sind ungültig. Da es sich hierbei um absolute Werte handelt, können Werte größer als 1,0f sein. Ein angemessener Grenzwert für "X", "Y" oder "Z". value ist willkürlich auf 10000.0f festgelegt.

### <a name="xyztype"></a>XYZType

Das XYZType-Element besteht aus drei IEEE-Gleitkommawerten mit einfacher Genauigkeit: "X", "Y" und "Z".

## <a name="the-cdmp-baseline-algorithms"></a>Die CDMP-Baselinealgorithmen

### <a name="crt-device-model-baseline"></a>CRT-Gerätemodellbaseline

Um dieses Modell zu verstehen, müssen Sie sowohl den Prozess der Bearbeitung als auch die Gerätemodellierung berücksichtigen. Im Rahmen des Vorgangs werden XYZ-Messungen zuerst für die Farben durchgeführt, die durch Auffüllen des Anzeigepuffers eines CRT-Anzeigegeräts abgerufen werden. Die folgenden Beispielwerte generieren gute Daten für das CRT-Basisgerätemodell:

Rot: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Grün: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blau: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutrale: R = G= B = 0, 8, 16, 32, 64, 128, 192, 255

Andere Inkremente als 15 und nicht lineare Inkremente können ebenfalls verwendet werden. Jede rote, grüne, blaue und neutrale Rampe muss mindestens drei Stichproben enthalten. Es wird jedoch empfohlen, weitere Stichproben bereitzustellen. Sie müssen Beispiele für reines Rot, Grün, Blau, Schwarz und Weiß bereitstellen. Die Stichproben müssen nicht gleichmäßig mit Leerzeichen getrennt werden.

Der Prozess zum Erstellen der tristimulus-Matrix besteht aus zwei Schritten. Schätzen Sie zunächst den Schwarzpunkt XYZ-Wert oder den Flare. Dieser Schritt basiert größtenteils auf der Arbeit vonUngs \[ 3 \] mit einer leicht geänderten Objective-Funktion für die nichtlineare Optimierung. Berechnen Sie zweitens die tristimulus-Matrix basierend auf dem Ergebnis aus Schritt 1 und auch aus einer Mittelwertberechnung für alle Pro-Kanal-Messungen, nicht nur die für die maximale digitale Anzahl.

Jeder dieser Schritte enthält ausführliche Verfahren. Der Ausgangspunkt sind die Rampen (in unserem Beispiel 17 Schritte) für jeden R-, G- und B-Kanal. Wenn die XYZ-Messungen auf der *xy-Ebene* der Scheitheit dargestellt werden, wird eine typische Situation in Abbildung 1 dargestellt. Schritt 1 besteht darin, ein nicht lineares Optimierungsproblem zu lösen, um den "am besten geeigneten" schwarzen Punkt zu finden, der die Abweichung in der Empfindlichkeit minimiert, während man die R-, G- und B-Kanäle durchläuft. Basierend auf Erfolgt \[ 3 \] suchen wir ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z <sub>K</sub>* ), um die folgende Zielfunktion zu minimieren:

![Zeigt die Objective-Funktion an, bei der Sr, Sg und Sb der Satz von Datenpunkten auf den R-, G- und B-Kanälen sind.](images/cdmp-formula1.png)

dabei sind *S <sub>R,</sub>**S <sub>G</sub>* und *S <sub>B</sub>* der Satz von Datenpunkten, die den Punkten auf den R-, G- und B-Kanälen entsprechen. Definieren Sie für alle S-Satzes Folgendes:

![Zeigt eine Formel zum Definieren eines beliebigen Satzes von S an.](images/cdmp-formula2.png)

Im vorherigen \| Beispiel ist *S* \| die Kardinalität von *S,* d.h. die Anzahl der Punkte in der Menge *S*. ![ Zeigt eine Formel für die Scheitigkeit eines Punkts an.](images/cdmp-formula3.png) ist die Scheitelpunktkoordinaten des Punkts ![ Zeigt eine Formaula für einen Punkt an.](images/cdmp-formula4.png) , also ![ Zeigt eine Formel für den Durchschnitt oder den Mittelpunkt der Massen an. ](images/cdmp-formula5.png) , ist der Durchschnitt oder Der Mittelpunkt der Massen aller Punkte in der Menge *S* in der Zentritätsebene. Zeigt daher ![ eine Formel für die Summe eines zweiten Punktmoments an.](images/cdmp-formula6.png) ist die Summe des zweiten Moments der Punkte über den Mittelpunkt der Massen und ein Maß dafür, wie weit die Punkte darüber verteilt sind. Schließlich ![ zeigt eine Formel für das Gesamtmaß der Verteilung von drei Punktclustern an.](images/cdmp-formula7.png) ist ein Gesamtmaß dafür, wie sich die drei Punktecluster auf die jeweiligen Massenzentren verteilen.

In der Berechnung von ![ Zeigt eine Formel von f(X,Y,Z; Xk, Yk, Zk).](images/cdmp-formula8.png) , wenn ![ eine Formel für X. ](images/cdmp-formula9.png) anzeigt, wird die Berechnung übersprungen, und die Kardinalität von *S* wird entsprechend angepasst.

Trotz der offensichtlichen Komplexität der Objective-Funktion ist es eine Summe aus den Quadraten vieler differenzierbarer Funktionen in *X <sub>K</sub>*,*Y <sub>K</sub>Z <sub>K</sub>* (17 Punkte 2 *xy* -Komponenten 3 Kanäle = 102 im Beispiel) und daher für standardmäßige techniken der geringsten Quadrate, z. B. den Levenberg-Marquardt Algorithmus, der in WCS verwendet wird. Beachten Sie, dass sich die vorherige Objective-Funktion von der in Erfolgt 3 empfohlenen \[ \] unterscheidet, da die letztere Funktion die Varianz der Entfernungen von der Mitte der Massen misst, sodass die Varianz null ist, wenn die Punkte vom Mittelpunkt der Massen gleich sind, obwohl sie sich recht stark darüber verteilen können. Im Beispiel wird die Menge der Punkte direkt mithilfe des zweiten Moments kontiert.

Wie bei jedem iterativen Algorithmus für das Problem der unlinearen kleinsten Quadrate erfordert Levenberg-Marquardt eine anfängliche Schätzung. Es gibt zwei offensichtliche Kandidaten. Eine ist (0, 0, 0); der andere ist der gemessene schwarze Punkt. Für den CTE wird der gemessene schwarze Punkt zuerst als anfangs erratener Wert verwendet. Wenn maximal 100 Iterationen überschritten werden, ohne einen Schwellenwert von durchschnittlich 0,001 von jedem Punkt vom Mittelpunkt der Massen zu erreichen (was einem Schwellenwert von (0,001) 17 3 = 0,000051 für die Zielfunktion entspricht), wird eine weitere Iterationsrunde mit der anfänglichen Schätzung von (0, 0, 0) ausgeführt. Die resultierende Schätzung des schwarzen Punkts ist XYZ im Vergleich zur besten Schätzung aus der vorherigen Iterationsrunde (mit dem gemessenen schwarzen Punkt als Anfangsschätzung). Verwenden Sie die Schätzung, die den kleinsten Wert für die Objective-Funktion angibt. Die Auswahl von 100 Iterationen und der Fehlerabstand von 0,001 wurden jeweils empirisch ausgewählt. In zukünftigen Versionen kann es sinnvoll sein, den Fehlerabstand zu parametrisieren.

Das Ergebnis von Schritt 1 ist der geschätzte schwarze Punkt ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z <sub>K</sub>* ). Schritt 2 besteht darin, die Tristimulusmatrix zu bestimmen, indem die Durchschnittlichkeit der Punkte in den drei Clustern ermittelt wird, die in Schritt 1 abgerufen wurden. Bei CRTs erfolgt dies in erster Linie, um die Auswirkungen von Messfehlern zu minimieren. Bei den Punkten, die im Mittel der Durchschnittlichkeit verwendet werden, muss es sich um die punkte, die in Schritt 1 in der Optimierung verwendet wurden, um identisch sein. Anders ausgedrückt: Wenn der erste Punkt (digitale Anzahl 15 im Beispiel) in jeder Rampe im Optimierungsschritt verworfen wird, muss dies auch im Mittelwert erfolgen. Wenn ![ Zeigt Formeln der gemittelten Scheitlichkeit für Koordinaten in den roten und grünen Kanälen an.](images/cdmp-formula10.png) und ![ Zeigt eine Formel der gemittelten Scheitlichkeit für Koordinaten im blauen Kanal an.](images/cdmp-formula11.png) sind die gemittelten Scheitchenkoordinaten der roten, grünen und blauen Kanäle. Anschließend bestimmt das folgende Verfahren die Tristimulusmatrix. Lösen Sie zunächst das lineare 3?3-System:

![Zeigt den ersten Teil der Prozedur zum Lösen eines linearen 3?3-Systems an.](images/cdmp-formula12.png)

![Zeigt den zweiten Teil des linearen 3?3-Systems an.](images/cdmp-formula13.gif)![Zeigt den Wert t subscript b am Ende des zweiten Teils des linearen 3?3-Systems an.](images/cdmp-formula14.gif)

*X <sub>W</sub>*,*Y <sub>W</sub>*,*Z <sub>W</sub>*

![Zeigt den letzten Teil der Prozedur zum Lösen eines linearen 3?3-Systems an.](images/cdmp-formula15.png)

Nachdem die Tristimulusmatrix bestimmt wurde, folgt die Bestimmung von Tonkurven dem Standardansatz. Bei CRT-Anzeigen wird davon ausgegangen, dass die einzelnen Kanäle dem GOG-Modell folgen:

![Zeigt die Formel für das G O G-Modell an.](images/cdmp-formula16.png)

wobei *k <sub>g</sub>* der "Gewinn", 1 –*k <sub>g</sub>* der "Offset" und ? ist das "Gamma". Die umgekehrte Matrix der tristimulus-Matrix wird auf die XYZ-Daten der Neutralen angewendet, um die linearen RGB-Daten zu erhalten, die dann mit den digitalen RGB-Werten korreliert werden, indem die nichtlineare Regression im GOG-Modell verwendet wird. Diese Merkmale müssen für die Kanäle R, G und B nicht identisch sein und sind im Allgemeinen nicht identisch.

Solls \[ 1 \] : Solls, *Bill dll und Saltzman es Principles of Color Technology*, 3 <sub>rd</sub> Ed. John Wiley & Sons (2000).

Listes \[ 2 \] : Senders and Solloh, The digital to radiometric transfer function for computer controlled CRT displays, *CIE Expert Symposium '97Lassliche Standards für Bildverarbeitungstechnologie,* November 1997.

Listes \[ 3 \] : Solls, Fernandez und Taplin, Estimating Black-Level Mission of Computer-Controlled Displays, *Color Research and Application,* 28: 379-383 Wiley Periodicals, Inc. (2003)

Kang \[ 1 \] : Kang, *Farbtechnologie für elektronische Bildverarbeitungsgeräte,* SPIE (1997)

Ungoh \[ 1 \] : Solloh, Deg dll undVals, Eine genaue Messung des CRT-Monitors (II) Vorschlag für eine Erweiterung der CIE-Methode und deren Überprüfung, *Opt. Rev.* 8: 397-408 (2001)

### <a name="lcd-device-model-baseline"></a>BASELINE für DAS GERÄTEMODELL

Die BASELINE für DAS GERÄTEMODELL ähnelt der CRT-Gerätemodellbaseline. In diesem Abschnitt werden die Unterschiede zwischen derTS-Modellierung und der CRT-Modellierung erläutert.

Ein Unterschied besteht in der Annahme, dass SIE nicht davon ausgehen können, dass DIE DISPLAYS dem gog-Modell folgen, das für CRTs verwendet wird, und dass die Tonkurven durch Interpolation der gemessenen Daten ermittelt werden. Daher sollte die geräteneutrale Achse häufiger entnommen werden.

Im Folgenden finden Sie einige typische Beispielwerte, die gute Daten für die BASELINE des MODELLS-Gerätemodells generieren können:

Rot: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Grün: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blau: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutral: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.

Der Prozess der Averagung gemessener Farbtoniken, um dieTicities für die Primärgeräte zu erhalten, ist für LCDs wichtiger als für CRTs. Wenn XYZ-Messungen auf der *xy-Ebene* der Heiterkeit dargestellt werden, wird in Abbildung 1 eine typische Situation dargestellt. Beachten Sie, wie sich dieTicity in Richtung des schwarzen Punkts abdrift. Dies liegt daran, dass alle LCDs eine bestimmte Menge an Lichtlecks haben.

![Diagramm, das ein Diagramm derTicity zeigt, in dem Rohdaten ohne Korrektur verwendet werden.](images/cdmp-lcd-dmp-figure1.png)

**Abbildung 1:** Das Diagramm mit derTicity mit Rohdaten ohne Korrektur

Wenn diese von den unformatierten XYZ-Messungen subtrahiert wird, wird eine typische Situation in Abbildung 2 dargestellt. Die Punkte werden nun in etwa drei Centern gruppiert, obwohl sie nicht identisch auf ihnen liegen. Der für CRTs beschriebene durchschnittliche Prozess verbessert die Ergebnisse für LCDs erheblich.

![Diagramm, das ein Diagramm derTicity zeigt, in dem Rohdaten mit einem angepassten schwarzen Punkt verwendet werden.](images/cdmp-lcd-dmp-figure2.png)

**Abbildung 2:** Das Diagramm mit derTicity mit Daten mit angepassten schwarzen Punkt

### <a name="rgb-capture-device-model-baseline"></a>RGB Capture Device Model Baseline

Das RGB-Basisgerätemodell ist eine Unterklasse der IDeviceModel-Klasse. In der Farbmetrik von Farberfassungsgeräten wie Scannern und Digitalkameras wird der folgende Ansatz verwendet. Ein Ziel, das aus Farbpatches mit bekannten CIEXYZ-Werten besteht, wird mithilfe des Erfassungsgeräts erfasst. Das Ergebnis der Erfassung ist ein RGB-Bitmapbild, in dem die Farbe jedes Patches in einem RGB-Wert codiert wird. Diese RGB-Gerätewerte sind spezifisch für ein bestimmtes Erfassungsgerät. Das Ziel der farbmetrikmetrischen Verfärbung besteht in der Einrichtung einer empirischen Beziehung zwischen den RGB-Werten des Geräts und CIEXYZ-Werten oder einer mathematischen Transformation von RGB zu XYZ, die das Verhalten des Erfassungsgeräts so genau wie möglich modelliert.

Eine solche mathematische Transformation kann angemessen durch Polynomen mit niedrigen Graden modelliert werden. Dieses Verfahren wird in der Fachdokumentation ausführlich beschrieben, z. B. Kang \[ 92 \] , Kang \[ 97 \] . In Kang 97 wird ein Ansatz gemeldet, bei dem eine Reihe von drei Polynomen mit den Begriffen \[ \] 3, 6, 8, 9, 11, 14 oder 20 in den Variablen R, G und B verwendet wird, während sich die drei Polynomen in die X-, Y- und Z-Komponenten des CIEXYZ-Raums zurückverteilen. Für das polynomiale 20-Term-Ausdruck hat die Form:

![Zeigt die 20-Term-Polynomie.](images/cdmp-formula20.png)

Es gibt ähnliche Ausdrücke für Y und Z. Die mathematische Technik für die Anpassung der Polynomen liegt innerhalb von "Multivariate Linear Regression" und wird in jedem elementaren Text in Statistics beschrieben.

Bei dieser Methode der linearen Regression wird die "richtige" Zielfunktion nicht minimiert. Die lineare Regression findet entwurfsweise die Lösung mit den geringsten Quadraten, was bedeutet, dass die erhaltenen Koeffizienten die Gesamtsumme der Quadrate von Fehlern im zugrunde liegenden Raum oder die Summe der Quadrate der euklidischen Entfernungen minimieren. In der Praxis möchten Sie die Summe der Quadrate von minimieren? Es, where ? E ist einer der akzeptierten Standards wie CIE94. Die Minimierung dieser Zielfunktion ist ein nicht lineares Regressionsproblem.

In der neuen Engine ist Lab to XYZ der CIE-Farbraum, in den regressiert wird, und das kubische Polynom mit 20 Begriffen wird als Modell für das Erfassungsgerät oder die Koeffizienten ls,as,bs verwendet, damit die folgenden Polynomen die Summe der Quadrate von minimieren? E <sub>CIE94</sub> s.

![Zeigt eine Reihe von polynomialen Formeln an.](images/cdmp-formula21.png)

Die Lösung ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) im 60-dimensionalen realen numerischen Raum **R** 203 muss so sein, dass der folgende Gesamtfehler minimiert wird:

![Zeigt den zu minimierenden Gesamtfehler an.](images/cdmp-formula22.png)

wobei die Summe durch alle Datenpunktpaare (*R <sub>i</sub>*,*G <sub>i</sub>*,*B i <sub>;</sub>**L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* ) im Beispieldatensatz sowie zusätzliche Kontrollpunkte, die im Folgenden ausführlich zu finden sind. Dies ist ein nicht lineares Regressionsproblem, da die Parameter *?<sub> i</sub>*, *ein <sub>i</sub>*, * <sub>i</sub>* geben in nicht linearer Weise (nicht quadratisch) in die Objective-Funktion ein.

Da die Objective-Funktion ? ist eine nicht lineare (und nichtquadratische) Funktion der Parameter *?<sub> i</sub>*, *ein <sub>i</sub>* und * <sub>i</sub>*. Sie müssen auf iterative Techniken zurück greifen, um das Optimierungsproblem zu lösen. Da die Form der Objective-Funktion eine Summe von Quadraten ist, wird eine Standardoptimierungstechnik verwendet, die Levenberg-Marquardt Algorithmus bezeichnet wird. Es wird als die Methode der Wahl für nicht lineare Probleme mit den geringsten Quadraten betrachtet. Für iterative Algorithmen wie z.B. Sollen-Marquardt müssen Sie eine erste Schätzung geben. Eine gute anfängliche Schätzung ist in der Regel wichtig, um den richtigen Mindestwert zu finden. In diesem Fall ist ein guter Kandidat für die anfängliche Schätzung die Lösung des linearen Regressionsproblems. Minimieren Sie zunächst die Summe der quadratischen Euklidischen Abstände im Laborraum, indem Sie eine quadratische Zielfunktion definieren:

![Zeigt eine definierte quadratische Zielfunktion an.](images/cdmp-formula23.png)

Die mathematische Lösung für ein solches Problem der "linearen geringsten Quadrate" ist bekannt. Weil *?<sub> i</sub>* wird nur in der *L-Modellierung* angezeigt, *ein <sub>i</sub>* wird nur in der *u-Modellierung* angezeigt, und * <sub>i</sub>* wird nur in der *v-Modellierung* angezeigt. Das Optimierungsproblem kann in drei Unterprobleme zersetzt werden: eines für *L,* eines für *u* und eines für *v*. Betrachten Sie die *L-Gleichungen.* (Die *u-Gleichungen* und *die v-Gleichungen* folgen genau demselben Argument.) Das Problem der Minimierung der Summe von Quadraten von Fehlern in *L* kann als Lösung der folgenden Matrixgleichung im Sinne der geringsten Quadrate angegeben werden:

![Zeigt eine Matrixgleichung für L.](images/cdmp-formula24.png)

wobei *N* die Gesamtzahl der Datenpunkte (ursprüngliche Stichprobenpunkte plus Kontrollpunkte, die auf die unten beschriebene Weise erstellt wurden) ist. In der Regel *ist N* viel größer als 20, sodass die obige Gleichung überbestimmt ist und eine Lösung mit den geringsten Quadraten erfordert. Eine geschlossene Formularlösung für **?** ist verfügbar:

![Zeigt eine geschlossene Formularlösung an.](images/cdmp-formula25.png)

In der Praxis wird die direkte Auswertung mithilfe der Lösung für geschlossene Formen nicht verwendet, da sie schlechte numerische Eigenschaften aufweist. Stattdessen wird eine Art Matrixfaktorisierungsalgorithmus auf die Koeffizientenmatrix angewendet, die das System der Gleichungen auf eine kanonische Form reduziert. In der aktuellen Implementierung wird SVD (Singular Value Decomposition) auf die **Matrix R** angewendet, und dann wird das resultierende zersetzte System gelöst.

Die Lösung für das lineare Regressionsproblem, die durch ![ Zeigt die Lösung für das lineare Regressionsproblem an.](images/cdmp-formula26.png) wird als Ausgangspunkt für den Levenberg-Marquardt verwendet. In diesem Algorithmus wird ein Testschritt berechnet, der den Punkt näher an die optimale Lösung verschieben sollte. Der Testschritt erfüllt eine Reihe von linearen Gleichungen, die vom Funktionswert und den Werten der Ableitungen zum aktuellen Zeitpunkt abhängig sind. Aus diesem Grund die Ableitungen der Objective-Funktion ? in Bezug auf die Parameter *?<sub> i</sub>*, *ein i <sub>i</sub> <sub>sind</sub>* erforderliche Eingaben für den Levenberg-Marquardt Algorithmus. Obwohl es 60 Parameter gibt, gibt es eine Verknüpfung, mit der Sie viel weniger berechnen können. Nach der Kettenregel des Calculus

![Zeigt eine Gleichung, die eine Verknüpfung mithilfe der Kettenregel von Calculus zulässt.](images/cdmp-formula27.png)

Dabei *ist j* = 1, 2, , 20, L *<sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* der CIELAB-Wert des *i.* Beispielpunkts, und *R <sub>ij</sub>* ist der (*i*,*j* )th-Eintrag der oben definierten **Matrix R.** Anstatt also Ableitungen für 60 Parameter zu berechnen, können Sie Ableitungen für *L,**a* und *b* mit numerischer Vorwärts-Differencing berechnen.

Es ist auch erforderlich, ein Beendigungskriterium für iterative Algorithmen zu einrichten. In der aktuellen Implementierung werden die Iterationen beendet, wenn das mittlere Quadrat DECIE94 kleiner als 1 ist oder die Anzahl der durchgeführten Iterationen 10 überschritten hat. Die Zahl 10 stammt aus der praxisorientierten Erfahrung: Wenn die ersten Iterationen den Fehler nicht erheblich reduzieren, helfen weitere Iterationen nur beim oszillativen Verschieben des Punkts, d. h. der Algorithmus kann nicht konvergieren. Auch wenn der Algorithmus ab weicht, können wir sicher sein, dass decie94 nicht schlechter als das ist, was wir gestartet haben, d. h. mit den Parametern, die aus der linearen Regression ermittelt wurden.

Selbst bei der vorherigen Methode der nicht linearen Regression gibt es mehrere Probleme mit der Anpassung. Ein Problem ist, dass die Polynomen tendenziell die Datenpunkte über- oder untergrenzen. Künstliche lokale Maxima und Minima können in den Anpassungsprozess eingeführt werden. Dies kann durch die Verwendung von Polynomen mit geringem Grad konstidiert werden. Dies ist der Grund, warum Sie nicht mehr als drei Grad verwenden sollten. Ein schwerwiegenderer Aspekt der Über- oder Unterschiefung ist, dass ein Polynom theoretisch jeden realen Wert an sich nehmen kann, aber der Zu modellierende Raum in der Regel physische Einschränkungen und praktische Einschränkungen auf sich hat. CIEXYZ muss alle X, Y, Z nicht negativ sein, was eine physische Einschränkung ist. In der Praxis nehmen sie nur Werte in der Größenordnung von Hunderten an, nicht Tausende oder höher. Ebenso gelten für CIELAB oder CIELUV eigene physische und praktische Einschränkungen. Wenn der RGB-Raum ausreichend mit Beispielpunkten gefüllt ist, ist das Problem der Über- oder Unterüberschreitung nicht schwerwiegend. Die erfassten RGB-Punkte des Erfassungsgeräts füllen den RGB-Raum jedoch in der Regel nicht einheitlich aus. Die Punkte füllen möglicherweise nur die inneren 80 % des RGB-Cubes aus, oder sie können sich in einem niedrigeren dimensionalen Würfel befinden. In diesem Fall können die zurückgeregten Polynomen schlechte Arbeit beim Extrapolieren der Werte über die Datenpunkte hinaus tun und manchmal unrealistische Vorhersagen zurückgeben. Sie möchten ein Modell, das immer einigermaßen realistische Werte zurückgibt. Dies erfordert eine Methode, die das Grenzverhalten von Regressionspolynomen effektiv steuern kann, indem den Polynomen, die sich in der Nähe der Grenze des RGB-Cubes erratisch verhalten, zusätzliche Kosten in Diesechen geht. Ein weiteres Measure, um sicherzustellen, dass die Polynomen immer realistische Werte zurückgeben, wird angewendet, indem die Ausgabe auf innerhalb des CIE-Locus abgeschnitten wird.

An diesem Punkt unterscheiden sich die Modellierung des Scanners und die Kameramodellierung voneinander. Es wird erwartet, dass das Kameramodell in Regionen außerhalb der Stichprobenpunkte einschließlich der "Glanzlichter" extrapoliert wird. Die gleiche Extrapolierung ist für das Scannermodell nicht erforderlich. Es wird erwartet, dass das Scannerziel eine 100000000000000000-30-000-30-000-30-000-30-000-30-0 Das Scannermodell muss in dem Sinne robust sein, dass es keine unrealistischen Werte zurückgeben sollte, aber eine Extrapolierung weit über das Ziel hinaus ist nicht erforderlich. Um die Stabilität sicherzustellen, wird das oben genannte L-Polynom bei 100 abgeschnitten, d.&160; das polynomische Modell wird gezwungen, nicht über "Dmin" des Scannerziels hinaus zu extrapolieren.

Es wird erwartet, dass das Kameramodell zu glanzförmigen Highlights extrapoliert wird, sodass das Ausschneiden bei 100 nicht erwünscht ist. Stattdessen wird der folgende Algorithmus verwendet.

Künstliche Kontrollpunkte werden eingeführt, um das Verhalten der Polynomen in Regionen mit unzureichender Stichprobenentnahme zu steuern. Indem diese Kontrollpunkte strategisch mit entsprechenden Werten platziert werden, dienen sie dazu, die Polynomen in die erforderliche Richtung zu "pullen". In der aktuellen Implementierung werden acht Kontrollpunkte verwendet, die den Ecken des RGB-Cubes entspricht. Wenn die Gerätewerte in Unity normalisiert werden, sind dies die folgenden Punkte:

*R* = 0, *G* = 0, *B* = 0

*R* = 0, *G* = 0, *B* = 1

*R* = 0, *G* = 1, *B* = 0

*R* = 0. *G* = 1, *B* = 1

*R* = 1, *G* = 0, *B* = 0

*R* = 1, *G* = 0, *B* = 1

*R* = 1, *G* = 1, *B* = 0

*R* = 1, *G* = 1, *B* = 1

Mit Ausnahme des weißen *R* G B = 1, der einem  =   =  CIELAB-Wert von *L* = 100, *u* v = 0 zugeordnet ist, wird der folgende  =  Extrapolationsalgorithmus verwendet, um den entsprechenden CIELAB-Wert zu bestimmen, dem zugeordnet werden soll. Im Allgemeinen wird für einen angegebenen (*R*,*G*,*B* ) jedem der (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) im Stichproben-DataSet eine Gewichtung zugeordnet. Es gibt zwei Ziele für die Zuweisung der Gewichtung. Erstens ist die Gewichtung umgekehrt proportional zum Abstand zwischen (*R*,*G*,*B* ) und (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ). Zweitens möchten Sie Punkte verwerfen oder Gewichtung 0 zuweisen, die einen anderen Farbton als der gegebene Punkt (*R,**G,**B ) haben.* Um den Farbton zu berücksichtigen, berücksichtigen Sie Punkte, die innerhalb eines Kegels liegen, dessen Scheitelpunkt sich bei (0, 0, 0) befindet, dessen Achse mit dem Verbinden der Linie (0, 0, 0) mit (*R*,*G*,*B* ) und dessen halb vertikalem Winkel zusammenfallen? erfüllt cos ? = 0,9. Eine Abbildung dieses Kegels finden Sie in Abbildung 3.

![Diagramm, das die Form der Umgebung zeigt.](images/cdmp-lcd-dmp-figure3.png)

**Abbildung 3:** Filtern der Beispielpunkte nach Winkel und Abstand. Die Form der dargestellten Umgebung dient nur zur Veranschaulichung. Die tatsächliche Form hängt von der verwendeten Entfernung ab. es ist eine rautenförmige Umgebung, wenn die 1-Norm verwendet wird.

Innerhalb dieses Kegels wird eine zweite Filterung durchgeführt, die auf der RGB-Entfernung basiert, die die von definierte 1-Norm verwendet.

![Zeigt die Formel für die zweite Filterung innerhalb des Kegels an.](images/cdmp-formula28.png)

Beim aktuellen Kegel wird zunächst nach Punkten gesucht, die sich in einem Abstand von 0,1 von (*R,**G,**B ) befinden.* Wenn innerhalb dieses Radius kein Punkt gefunden wird, wird der Radius um 0,1 erhöht, und die Suche wird neu gestartet. Wenn die nächste Runde auch keinen Punkt hat, wird der Radius um 0,1 erhöht. Dieser Prozess wird fortgesetzt, bis der Radius MaxDist/5 überschreitet, wobei MaxDist = 3 im Fall von 1 Norm ist. Wenn kein Punkt gefunden wird, wird der Kegel vergrößert, indem das Cos verringert wird? um 0,05, d.&a; erhöhung des Winkels ? und neustarten den gesamten Prozess mit einem zunehmenden Radius. Dieser Prozess wird fortgesetzt, bis ein nicht leerer Satz von Punkten gefunden wird oder cos ? erreicht 0, d.&a; der Kegel hat sich geöffnet, um eine Ebene zu werden. An diesem Punkt wird die Suche neu gestartet, indem der Radius erhöht wird, mit der Ausnahme, dass die Suche fortgesetzt wird, bis der Radius MaxDist erreicht. Dadurch wird sichergestellt, dass im ungünstigsten Fall ein nicht leerer Satz von Punkten gefunden wird. Der Algorithmus wird im Flussdiagramm in Abbildung 4 zusammengefasst.

![Diagramm, das den Fluss des Algorithmus zeigt.](images/cdmp-lcd-dmp-figure4.png)

**Abbildung 4:** Flow Diagramm zum Bestimmen des Sets S von Beispielpunkten, die in der Extrapolation für einen RGB-Eingabewert verwendet werden

Angenommen, der vorherige Prozess ergibt einen nicht leeren Satz *von Punkten* (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) und entsprechende (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), dann wird für jeden solchen Punkt eine Gewichtung *w <sub>i</sub>* zugewiesen, angegeben durch

![Zeigt die Formel für eine Gewichtung für jeden Punkt an.](images/cdmp-formula29.png)

Schließlich wird der Extrapolant durch definiert.

![Zeigt die Definition für den Extrapolanten an.](images/cdmp-formula30.png)

Die vorangehenden Gleichungen bilden eine Instanz der "inverse entfernungsgewichteten Methoden", die häufig als Shepard-Methoden bezeichnet werden. Indem jeder der acht Punkte von eq (6) über den Algorithmus ausgeführt wird, werden acht Kontrollpunkte mit *R,G,**B* und *L,**a*,*b-Werten,* die mit den ursprünglichen Beispieldaten in den Pool eingedrung werden, ermittelt.

Um sicherzustellen, dass das Modell immer gültige Farbwerte erzeugt und die Systemintegrität und -stabilität in der gesamten Farbverarbeitungspipeline gewährleistet ist, müssen Sie eine abschließende Beschneidung der Ausgabe des polynomialen Modells durchführen. Der allgemeine CIE-Visual-Gamut wird von der aischen Komponente (*Y* oder *L* ) und dertic-Komponente (*xy* oder *a'b'*) beschrieben, die durch eine projektive Transformation mit dem XYZ-Raum verknüpft sind. In der aktuellen Implementierung wird die *a'b'-Ticity* verwendet, da sie direkt mit dem CIELUV-Raum verknüpft ist. Legen Sie *für jeden CIELAB-Wert* *zuerst L auf* einen nicht negativen Wert ab:

![Zeigt die Beschneidung von L auf einen nicht negativen Wert an.](images/cdmp-formula31.png)

Um die Extrapolierung für glanzförmige Highlights zu ermöglichen, wird *L* nicht bei 100 abgeschnitten, der "konventionellen" Obergrenze für *L* im Laborbereich.

Wenn als Nächstes *L* = 0 ist, werden *a* und *b* so abgeschnitten, dass a =*b =* 0 ist. Wenn *L* ? 0, berechnen

![Zeigt die Formel an, wenn L=0 ist.](images/cdmp-formula32.png)

Dies sind die Komponenten eines Vektors im *a'b'-Diagramm* aus dem Weißpunkt (*u?'*,*v?'* ) in der in Frage gestellten Farbe. Definieren Sie den CIE-Locus als konvexe Hülle aller Punkte *(a'*,*b'* ), parametrisiert durch die Hülle ?:

![Zeigt die Formel für die Unterschiedliche an.](images/cdmp-formula33.png)

wobei ![ zeigt die Funktionen für den CIE-Farbabgleich an.](images/cdmp-formula34.png) sind die CIE-Farbvergleichsfunktionen für den 2-Grad-Beobachter. Wenn sich der Vektor außerhalb des CIE-Locus befindet, wird die Farbe an den Punkt auf dem CIE-Locus abgeschnitten, der die Schnittmenge des Locus und der durch den Vektor definierten Linie darstellt. Weitere Informationen in Abbildung 5. Wenn ein Clipping erfolgt ist, werden *die Werte a* und *b* rekonstruiert, indem zuerst ein subtrahiert *wird?* und *b?* aus dem *abgeschnittenen a'* und *b'*, und multipliziert dann mit 13 *L*.

![Diagramm, das das Diagramm für den Clippingalgorithmus zeigt.](images/cdmp-lcd-dmp-figure5.png)

**Abbildung 5:** Beschneidungsalgorithmus für Lab-Werte, die sich außerhalb des visuellen Gamuts des CIE-Visuals befinden

In der aktuellen Implementierung wird der CIE-Locus in der *a'b'-Ebene* durch eine stückweise lineare Kurve mit 35 Segmenten dargestellt (entspricht einem 360-Nm-Wert bis einschließlich 700 nm). Durch die Sortierung der Liniensegmente, sodass ihre unterbeaufsichtigten Winkel am weißen Punkt aufsteigend sind, was absteigenden Strichen entspricht, kann das Liniensegment, das sich mit dem vom obigen Vektor gebildeten Strahl überschneidet, durch eine einfache binäre Suche gefunden werden.

### <a name="rgb-printer-device-model-baseline"></a>RGB-Drucker– Gerätemodellbaseline

Ein Gerätekonstrukt eines RGB-Druckers besteht aus der Konstruktion eines empirischen Modells des Geräts, das die geräteunabhängige CIELUV-Farbe für einen bestimmten RGB-Wert vorhersagt.

Es gibt zwei Möglichkeiten, das empirische Modell zu erstellen. Eine Möglichkeit ist die Verwendung der Gerätedaten für einen RGB-Drucker und die andere die Verwendung analytischer Parameterdaten. Im ersten Beispiel werden von einem Benutzer für ein RGB-Druckergerät bereitgestellte Messdaten verwendet, um eine 3D-Nachschlagetabelle (3D Lookup Table,KONSTRUKT) zu erstellen. Die Messdaten bestehen aus XYZ-Werten für RGB-Patches mit gleichmäßiger Stichprobenentnahme. Typische Stichprobengrößen sind 9 oder 17 für jede Komponente. Jeder Patch wird mit einem Farbbereich oder spectrophotometer im CIEXYZ-Raum gemessen. Der XYZ-Wert für einen Patch wird dann in einen CIELUV-Wert konvertiert, der ein 3D-FORMULAR bildet. Im Gerätemodell wird die 3D-Interpolationsmethode von Sakaaka zur Vorhersage der CIELUV-Daten für eine bestimmte RGB-Daten auf die 3D-Interpolationsmethode angewendet. (Us Patent 4275413 (Sakaaka et al.), US Patent 4511989 (Sakaaka), Kang \[ 1 \] . Die beiden Erwähnten sind abgelaufen.) Bei den analytischen Parameterdaten, die in der zweiten Methode übergeben werden, handelt es sich einfach um ein zuvor erstelltes DANN. In der Regel wurde diese WIEGE mit der ersten Methode erstellt, obwohl sie von Hand erstellt werden konnte.

In der aktuellen Farbverwaltung wird die Quellkarte als die Karte definiert, die vom RGB-Raum zu einem geräteunabhängigen CIEXYZ-Farbraum geht. Die Zielkarte ist als die Karte definiert, die vom geräteunabhängigen CIEXYZ-Farbraum in den RGB-Raum übergeht. Dies ist die Umkehrung der Quellzuordnung.

Das empirische Modell wird direkt in der Quellzuordnung verwendet. Sie ordnet zunächst eine bestimmte RGB-Daten einer CIELUV-Daten zu, die in XYZ-Daten konvertiert werden. In der Zielzuordnung werden geräteunabhängige CIEXYZ-Daten zuerst in CIELUV-Daten konvertiert. Anschließend werden das empirische Modell und die klassische Newton-Raphson verwendet, um die besten RGB-Daten für die CIELUV-Daten vorherzusagen. Die Details zur Konvertierung von CieLUV- in RGB-Daten lauten wie folgt:

Nach der Generierung eines 3D-3D-3D-3D-NS von RGB zu CieLUV wird die Zuordnung von RGB zu LUV mithilfe der linearen Interpolation in RGB erstellt. Diese Zuordnung wird durch die folgenden Gleichungen bezeichnet:

![Zeigt die Gleichungen für die Zuordnung von R G B zu L U V.](images/cdmp-image125.png)

Die Umkehrung der Karte besteht aus der Lösung für jede Farbe. ![Zeigt L U V an.](images/cdmp-image127.png) , das folgende System von nicht linearen Gleichungen:

![Zeigt die nicht linearen Gleichungen zum Lösen einer beliebigen Farbe L U V.](images/cdmp-image129.png)

Eine nicht lineare Gleichung, die auf der klassischen Newton-Raphson basiert, wird im neuen CTE verwendet. Eine anfängliche Schätzung oder *a priori* see s <sub>prior</sub> -(R 0, G 0, B 0 ) wird durch Durchsuchen einer "Seedmatrix" ermittelt, die aus einem 8x8x8-Raster mit vorab berechneten (RGB,Luv)-Paaren besteht. Die RGB-entsprechende Luv, die der L u v am nächsten \* \* \* liegt, wird ausgewählt. Jeder Punkt in der Startmatrix entspricht dem Mittelpunkt einer Zelle, sodass die Iterationen nicht mit einem Punkt auf der Begrenzungsgesicht des RGB-Cubes beginnen. Anders ausgedrückt: Die RGB-Werte der Seeds werden durch: STEP = 1/8 s <sub>bzw.</sub> (STEP/2 + (i-1) STEP, STEP/2+(j-1)STEP, STEP/2+(k-1)STEP) mit i,j,k = 1...8 Im *ersten* Schritt von Newton-Raphson zeigt die nächste Schätzung die Variablen für die nächste Schätzung ![ an.](images/cdmp-image133.png) wird von der Formel erhalten:

![Zeigt die Formel für die Schätzung an.](images/cdmp-image135.png)

Die Iteration wird beendet, wenn der Fehler (Abstand im CIELUV-Raum) kleiner als eine vorab festgelegte Toleranzstufe (0,1 im CTE) ist oder wenn die Anzahl der Iterationen die maximal zulässige Anzahl von Iterationen (10 im CTE) überschritten hat. Die Werte für die Toleranz und die Anzahl der Iterationen wurden empirisch als effektiv bestimmt. In zukünftigen Versionen kann der Toleranzwert geändert werden.

Die feldische Matrix wird mithilfe der Vorwärtsdifferenz berechnet, mit Ausnahme eines Begrenzungspunkts (mindestens einer der R-, G- und B-Werte ist 1), an dem stattdessen die Abwärtsdifferenz verwendet wird. Anstatt die Umkehrung derIgen-Matrix zu berechnen, wird das lineare System direkt mithilfe der Gauss-Jordan mit vollständiger Pivotierung gelöst.

Am Ende der Iterationen wird die Konvergenz möglicherweise immer noch nicht erreicht, da Newton-Raphson ein "lokaler" Algorithmus ist. Das heißt, er funktioniert nur gut, wenn Sie mit einer anfänglichen Schätzung beginnen, die der tatsächlichen Lösung nahe kommt. Wenn am Ende der Newton-Raphson Iterationen keine Konvergenz innerhalb der vordefinierten Fehlertoleranz erreicht wurde, werden die Iterationen mit einem neuen Satz von Startkernen neu gestartet, der wie folgt definiert ist.

Die bisher beste Lösung ist beispielsweise (r, g, b). Aus dieser Lösung werden N posteriori-Kerne abgeleitet, wobei N = 4 ist. Intuitiv wird die Lösung in einer Schrittgröße, die von N abhängt, "in richtung Mitte" verschoben. Siehe Abbildung 6.

![Diagramm mit Denkrichtungen der Lösung.](images/cdmp-image136.png)

**Abbildung 6:** Die Richtung der Kippung der Lösung hängt davon ab, in welchem Oktett sie sich befindet.

Anders ausgedrückt: Wenn r 0,5 ist, wird der Wert im &gt; R-Kanal verringert, andernfalls wird der Wert erhöht. Es gibt eine ähnliche Logik für die Kanäle G und B. Die genauen Definitionen sind:

PERTURBATION = 0,5/(N+1)

Dir(r) = -1, wenn r &gt; 0,5; andernfalls +1. Auf ähnliche Weise für Dir(g) und Dir(b)

Der jth a posteriori seed, s ????, is (r + Dir(r) \* j \* PERTURBATION, g + Dir(g) \* j \* PERTURBATION, b + Dir(b) \* j \* PERTURBATION)

Probieren Sie die ersten ???? Und wenn es eine neue Lösung innerhalb der Fehlertoleranz gibt, können Sie beenden. Versuchen Sie andernfalls die zweite ???? und so weiter, bis der N-????.

Die Schemata des gesamten Algorithmus sind in Abbildung 7 dargestellt.

![Diagramm, das den Ablauf für die Invertierung des Gerätemodells zeigt.](images/cdmp-image138.png)

**Abbildung 7:** Schemata zur Invertierung des Gerätemodells

### <a name="rgb-virtual-device-model-baseline"></a>RGB-Modellbaseline für virtuelle Geräte

Dieses Gerätemodell (DEVICE Model, DM) ist ein einfacher Algorithmus zur Matrix-/Tonwiedergabe. Die Matrix wird mithilfe von Color Science-Standardalgorithmen vom Weißen Punkt und den Primärfarben abgeleitet. Die Tonwiedergabekurve wird von den Messparametern gemäß den BESCHREIBUNGen von CURVEType und ParametricType abgeleitet (oder bei Bedarf umgekehrt). Details zu den internen Algorithmen werden nach der zusätzlichen Validierung von Problemen mit hohem dynamischen Bereich bereitgestellt.

Das MODELL des virtuellen RGB-Geräts ist eine idealisierte Matrix-/Tonwiedergabekurve RGB, die dem MATRIX-basierten Profilentwurf mit drei Komponenten in FORM VON RGB ähnelt. Zu den Parametern der "virtuellen Messung" der DM gehören ein Weißpunktwert (absolute CIEXYZ), RGB-Primärwerte (absolute CIEXYZ) und eine Tonabbildungskurve, die auf dem PARAmetricCurveType- und CurveType-Wert für die XML-Formatierung basiert, die mit den DMP-Schemas konsistent ist.

DIE PARAMETRICCurveType-Funktionstypcodierung und die entsprechende Unterstützung in IRGBVirtualDeviceModelBase sind in der folgenden Tabelle aufgeführt.



| Funktionstyp                                         | Parameter                          | type                                     | Hinweis                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Zeigt die GammaType-Funktion an.](images/cdmp-image154.png)<br/> | g<br/>              | GammaType<br/>                 | Allgemeine Implementierung<br/>           |
| ![Zeigt die GammaOffsetGainType-Funktion an.](images/cdmp-image156.png)<br/> | ga b<br/>           | GammaOffsetGainType<br/>       | CIE 122-1966<br/>                    |
| ![Zeigt die GammaOffsetGainOffsetType-Funktion an.](images/cdmp-image158.png)<br/> | ga b c<br/>         | GammaOffsetGainOffsetType<br/> | IEC 61966-3<br/>                     |
| ![Zeigt die GammaOffsetGainGainType-Funktion an.](images/cdmp-image160.png)<br/> | ga b c d<br/>       | GammaOffsetGainGainType<br/>   | IEC 61966-2.1<br/> (sRGB)<br/> |
| ![Zeigt eine Funktion für "g a b c d e f"-Parameter an.](images/cdmp-image162.png)<br/> | ga b c d e f<br/>   | Nicht zutreffend<br/>                       | In WCS nicht unterstützt<br/>            |



 

Die Tonkurve für virtuelle RGB-Geräte wird in DeviceToColorimetric zwischen den Eingabedaten, pDeviceColors und der Matrixmultiplikation angewendet. Für ColorimetricToDevice muss eine Methode verwendet werden, um die Tonkurve umzudrehen. In der Baselineimplementierung erfolgt dies durch direkte Interpolation in derselben Tonkurve, die für DeviceToColorimetric verwendet wird.

Die Kurven sollten in den Profilen als Zahlenpaare im Gleitkommabereich angegeben werden. Die erste Zahl stellt Werte in pDeviceColors dar. Die zweite Zahl stellt die Ausgabe der Tonkurve dar. Alle Werte in der Tonkurve müssen zwischen minColorantUsed und maxColorantUsed liegen. Tonkurven müssen mindestens zwei Einträge enthalten: einen für minColorantUsed und einen für maxColorantUsed. Die maximale Anzahl von Einträgen in ToneCurve beträgt 2048. Im Allgemeinen gilt: Mit mehr Einträgen in der Tabelle können Sie die Krümmung genauer modellieren. Zwischen den Einträgen wird eine stückweise lineare Interpolation ausgeführt.

Sie können alternative Interpolationsmethoden in Betracht ziehen. Wenn Sie etwas über das zugrunde liegende Verhalten des Geräts wissen, können Sie weniger Stichproben verwenden und mit einer Kurve höherer Ordnung genauer modellieren. Wenn Sie jedoch den falschen Kurventyp verwenden, sind Sie sehr ungenau. Ohne weitere Informationen können Sie den Kurventyp nicht erraten. Verwenden Sie also lineare Interpolation, und stellen Sie viele Datenpunkte zur Verfügung.

### <a name="cmyk-printer-device-model-baseline"></a>Modellbaseline des CWERT-Druckergeräts

Eine Geräteinserierung eines CKONSTRUKT-Druckers besteht aus der Konstruktion eines empirischen Modells des Geräts, das die gedruckte Farbe für jeden angegebenen CKONSTRUKT-Wert vorhersagt. Die Enumerierung umfasst auch die Umkehrung dieses Modells, sodass eine Verzweigung des C WIE-Werts für eine bestimmte Farbe, die gedruckt werden soll, angegeben werden kann. Dies wird in der Regel als CIEXYZ- oder CIELAB-Wert definiert.

In der Regel wird ein IT8.7/3-Ziel verwendet, das C PATCH-Patches enthält. Die Patches bestehen aus einer stichprobenbasierten Stichprobenentnahme des CSTELLUNG-Bereichs in einer klar definierten Weise, sodass ein rechteckiges Raster (mit nicht einheitlichem Abstand in C, M, Y und K) gebildet wird. Jeder Patch wird dann mit einem Farbbereich oder Spectrophotometer gemessen. Die Messungen in CIEXYZ-Werten bilden dann eine Nachschlagetabelle (LOOK), aus der mithilfe der Interpolationsmethode von Sakaaka ein empirisches Modell des Druckers erstellt wird. US Patent 4275413 (Sakaaka et al.), US Patent 4511989 (Sakaaka), Kang \[ 1 \] . Die beiden erwähnten Lizenzen sind abgelaufen.

Es gelten die folgenden spezifischen Anforderungen für die C BASELINE-Messbeispiele, die erforderlich sind, damit ein Gerätemodellprofil vom C BASELINE-Gerätemodell als gültig akzeptiert wird. (Der Beispielsatz wird am deutlichsten als eine Gruppe von CMY-Beispielcubes beschrieben, die jeweils einer bestimmten K-Ebene zugeordnet sind.)

-   Für die Ebenen K = 0 und K = 100 müssen mindestens gültige CMY-Cubes bereitgestellt werden.
-   Zwischen-K-Ebenen können nicht einheitlich leerzeichen.
-   Alle K-Zwischenebenen ohne gültigen CMY-Cube werden ignoriert.
-   Die CMY-Cubes verwenden möglicherweise nicht einheitliche Stichprobenintervalle (Rasterabstand), aber für eine bestimmte K-Ebene müssen in allen C-, M- und Y-Dimensionen im CMY-Cube die gleichen Stichprobenintervalle verwendet werden.
-   Jeder CMY-Cube auf K-Ebene kann eine andere Anzahl und einen anderen Abstand von Stichprobenintervallen verwenden.
-   Alle CMY-Cubes müssen die "Ecken" des CMY-Cubes enthalten. Das heißt, CMY-Beispiele bei \[ 0,0,0, \] \[ 0,0,100, \] \[ 0,100,0, \] \[ 100,0, \] \[ 0,100,100, \] \[ 100,0,100 \] , \[ 100,100, 0 \] , \[ 100,100,100 \] .
-   Alle CMY-Zwischenrasterebenen müssen in jedem Kanal vollständig entnommen werden. Anders ausgedrückt: Eine Stichprobe muss an jeder 3D-Rasterschnittmenge innerhalb des CMY-Cubes vorhanden sein.
-   Für die Cubes K = 0 und K = 100 CMY sind 2x2x2 "nur Ecken"-Cubes die minimal akzeptierten gültigen Cubes.

    \[HINWEIS: Bei K=0- und K=100-Ebenen wird ein 3x3x3 CMY-Cube als 2x2x2-Cube verarbeitet, der nur Ecken enthält. die Zwischenstichprobenebene wird ignoriert. Bei 4 x 4 x 4 und größeren Cubes werden alle Stichproben im Raster verwendet.\]

-   Für K-Zwischenebenen sind 4 x 4 x 4 CMY-Cubes die minimal akzeptierten gültigen Cubes.

Für ein Profil mit hoher Qualität werden feiner als für die Gültigkeit erforderliche Stichprobenraster verwendet( in der Regel 9 x 9 x 9 x 9 oder höher). Die Beispiele aus den Zielen IT8.7/3, IT8.7/4 und ECI erzeugen gültige Gerätemodellprofile (DEVICE Model Profiles, DMPs) für das C BASELINE-Gerätemodell des Druckers. Dieses Gerätemodell kann zwar die zusätzlichen (off-grid)-Stichproben in diesen Zielen ignorieren, aber es ist nicht garantiert, dass es dies für andere Ziele tun kann. Daher wird empfohlen, dass zusätzliche Stichproben aus Messsätzen entfernt werden, die in Profile für dieses Gerätemodell übertragen werden.

Die Umkehrung des Druckermodells führt zu mehr Schwierigkeiten. Bei einer Eingabefarbe in CIECAM gibt es eine Frage, ob diese Farbe innerhalb des Drucker-Gamuts liegt. Es gibt auch das Problem in Bezug auf die Anordnung von Punkten im Farbbildraum. Obwohl wir die CSTELLUNG-Werte so anordnen können, dass sie auf ein rechteckiges Raster fallen, wie dies im IT8.7/3-Ziel der Fall ist, kann nicht dasselbe über die resultierenden gedruckten Farben gesagt werden, wie sie im Farbbildraum dargestellt werden. Im Allgemeinen sind sie im Farbbildbereich ohne bestimmtes Muster verteilt.

Im Allgemeinen gibt es zwei Ansätze für das Problem der Umkehrung von Punktdiagrammen. Ein Ansatz ist die Verwendung einer geometrischen Unterteilung des Druckers gamut mit elementaren 3-dimensionalen Festkörpern, z. B. einer Klammerdra. Eine Unterteilung der Drucker gamut im Farberscheinungsbildbereich kann aus der entsprechenden Unterteilung des CMY(K)-Raums abgeleitet werden. Weitere Informationen finden Sie unter Hung \[ 93 \] , Kang \[ 97 \] . Dieser Ansatz hat den Vorteil der Einfachheit der Berechnung. Im Fall eines Zyhedrons werden nur vier Punkte in einer Interpolation verwendet. Andererseits hängt das Ergebnis stark von einigen Punkten ab, was bedeutet, dass ein Messungsfehler erhebliche Auswirkungen auf das Ergebnis hat. Die Interpolant ist in der Regel auch nicht so reibungslos. Der zweite Ansatz geht nicht von einer Unterteilung aus und basiert auf der Technik der Punktdateninterpolation. Ein klassisches Beispiel ist die Technik der Shepard-Interpolation oder umgekehrt gewichteten Methode (siehe Shepard \[ 68 \] ). Hier werden mehrere Punkte, die den Eingabepunkt umgeben, in irgendeiner Weise ausgewählt, jedem eine Gewichtung zugewiesen, in der Regel umgekehrt proportional zur Entfernung, und der Interpolant wird als gewichteter Durchschnitt der benachbarten Punkte verwendet. Bei diesem Ansatz ist die Auswahl benachbarter Punkte von entscheidender Bedeutung für die Leistung. Obwohl zu wenige Punkte die interpolanten ungenauen und nicht reibungslosen Ergebnisse rendern können, verursachen zu viele Punkte hohe Berechnungskosten, da die Gewichtungen in der Regel nicht lineare Funktionen und kostspielige Computefunktionen sind.

Die beiden oben beschriebenen Ansätze haben Probleme. Der Unterteilungsansatz hängt entscheidend davon ab, dass die Daten relativ rauschend sind, und die Interpolation ist im Allgemeinen nicht sehr reibungslos. Die Punktdateninterpolation ist gegenüber Datenrauschen toleranter und bietet im Allgemeinen eine reibungslosere Interpolation, ist aber rechenintensiver.

Der neue CTE verfolgt einen alternativen Ansatz. Das CASSO-Gerät wird als Sammlung mehrerer CMY-Geräte behandelt, von denen jedes über einen bestimmten Wert von schwarz (K) verfügt. Mithilfe eines Auswahlalgorithmus, der als Parameter lightness und lightness verwendet, wird eine Ebene schwarz ausgewählt. Die CMY-Werte werden durch Die Umkehrung der entsprechenden CMY-zu-Luv-Tabelle mithilfe der Newton-Methoden ermittelt, die an anderer Stelle vom RGB-Druckeralgorithmus verwendet werden.

Führen Sie die folgenden Schritte aus.

1.  Geben Sie das Ziel aus, bei dem es sich entweder um das IT8.7/3-Ziel oder um ein Ziel handelt, das in regelmäßigen oder unregelmäßigen Abstandsintervallen Stichproben des C SAMPLING-Raumes enthält.
2.  Messen Sie das Ziel mithilfe eines Spectrophotometers, und konvertieren Sie die Messungen in den CIELUV-Raum.
3.  Erstellen Sie die Vorwärtszuordnung von CZUORDNUNG zu Luv.
4.  Verwenden Sie die Vorwärtszuordnung, um einen Satz von CMY-zu-Luv-Karten für einen Bereich von K-Werten zu erstellen.
5.  Für jeden Luv-Eingabewert wird der entsprechende CZUORDNUNG-Wert ermittelt, indem eine der in Schritt 4 oben erstellten Karten ausgewählt und die Newton-Methode verwendet wird, um einen CMY-Farbsatz zu erhalten, der den ausgewählten K-Wert begleitet.

Die Schritte 1 und 2, bei denen es sich um Standardverfahren handelt, werden von einem Profilerstellungsprogramm ausgeführt, das nicht Teil des neuen CTE ist. Das IT8.7/3-Ziel enthält eine einigermaßen detaillierte Stichprobenentnahme aller CPROBE-Werte auf verschiedenen Ebenen von C, M, Y und K. Alternativ kann ein benutzerdefiniertes Ziel mit einheitlicher Stichprobenentnahme der Kanäle C, M, Y und K verwendet werden. Nachdem das Ziel gedruckt wurde, kann ein Spectrophotometer oder Farbbereich verwendet werden, um den XYZ-Wert jedes Patches zu messen, und der XYZ-Wert kann mithilfe des CIELUV-Modells in den Luv-Wert konvertiert werden.

Schritt 3: Die Konstruktion der Vorwärtszuordnung von CSTELLUNG zu Luv kann durch Anwenden einer bekannten Interpolationstechnik, z. B. einer gekachelten oder mehrlinearen Methode, auf das rechteckige Raster im CFÜ-Raum erreicht werden. Im neuen CTE wird eine vierdimensionale dimensionsbasierte Interpolation verwendet. Da sich die CMY-Stichprobenraster in der Regel auf jeder K-Ebene unterscheiden, verwenden wir eine Technik der Superstichprobe, wie unten beschrieben. Für einen bestimmten C STANDARDWERT-Punkt werden die Sandwiching-K-Ebenen zuerst basierend auf dem K-Wert bestimmt. Führen Sie dann ein "Superraster" auf jeder K-Ebene ein, das eine Vereinigung der CMY-Raster auf jeder der beiden K-Ebenen ist. Auf jeder K-Ebene wird der Luv-Wert eines neu eingeführten Rasterpunkts durch eine dreidimensionale dimensionsbasierte interpolation innerhalb dieser K-Ebene ermittelt. Schließlich wird in diesem neuen Raster eine vierdimensionale interpolierte Interpolation für den spezifischen CFÜ-Punkt ausgeführt.

![Diagramm, das die Supersampling zeigt.](images/cdmp-image163.png)

**Abbildung 8:** Supersampling

Schritt 4 erstellt einen Satz von CMY-zu-Luv-Suchtabellen (LUTs). Die in Schritt 3 konstruierte Vorwärtszuordnung wird wiederholt aufgerufen, um den CMAP-Raum erneut zusammpeln. Der CUNION-Farbraum wird mit einem gleichmäßigen Abstand von K und einer anderen, aber immer noch gleichmäßigen Stichprobenentnahme von CMY entnommen.

Schritt 5 ist eine Prozedur zum Abrufen des CKONSTRUKT-Werts mithilfe der in Schritt 4 erstellten LUTs für einen beliebigen Luv-Eingabepunkt. Der entsprechende Wert von K wird ausgewählt, indem die Lichtheit sowie der Farbgrad in der angeforderten Luv analysiert werden. Nachdem die Tabelle ausgewählt wurde, werden die CMY-Werte mithilfe der Newton-Methode aus der Tabelle ermittelt (wie weiter oben im RGB-Druckergerätemodell dokumentiert).

CIELUV-Speicherplatz wird im Druckermodell anstelle von CIEJab verwendet, da das Gerätemodell ausschließlich auf farbmetrikmetrischen Daten basieren sollte, die im DMP verfügbar sind. Der DMP enthält Farbmetrikdaten für jeden gemessenen Patch, einschließlich des Medien-Weißpunkts, sodass es möglich ist, CIEXYZ-Daten in CIELUV-Daten zu konvertieren. Es ist jedoch nicht möglich, in CIECAM02 JCh oder Jab zu konvertieren, da kein Zugriff auf die Anzeigebedingungsinformationen im DMP besteht.

### <a name="rgb-projector-device-model-baseline"></a>RGB-Projektor– Gerätemodellbaseline

Hinweis: Viele RGB-Projektoren verfügen über mehrere Betriebsmodus. In einem Modus, der häufig die Standardeinstellung ist und beispielsweise als "Präsentation" bezeichnet werden kann, ist die Farbantwort des Projektors für maximale Helligkeit optimiert. In diesem Modus verliert der Projektor jedoch die Fähigkeit, helle, leicht lässige Farben zu reproduzieren, wie z. B. gelben Gelben und einigen Tönen. In einem anderen Modus, der häufig als "Film", "Video" oder "sRGB" bezeichnet wird, ist der Projektor für die Wiedergabe realistischer Bilder und natürlicher Szenen optimiert. In diesem Modus wird die maximale Helligkeit abgeschaltet, um die Gesamtqualität der Farbwiedergabe zu verbessern. Um eine zufriedenstellende Farbwiedergabe mit RGB-Projektoren zu erhalten, ist es erforderlich, den Projektor in einem Modus zu platzieren, in dem eine gleichmäßige Farbpalette reproduziert werden kann.

![Diagramm, das ein D L P-Gerätemodell zeigt.](images/cdmp-image167.png)

**Abbildung 9:** DLP-Gerätemodell

Ein eingehender RGB-Wert durchläuft zwei Berechnungspfade. Das erste ist das Matrixmodell, das zu einem XYZ-Wert führt. Unmittelbar darauf folgt die Konvertierung von XYZ in Luv. Die zweite ist die nicht einheitliche INTERPOLation VON INTERPOLATION mithilfe der interpolierten Interpolation . Die Ausgabe der Interpolation befindet sich durch Konstruktion bereits im Luv-Raum. Die beiden Ausgaben werden hinzugefügt, um den vorhergesagten Luv-Wert zu erhalten. Dies wird schließlich in XYZ konvertiert. Dies ist die erwartete Ausgabe des Farbmetrikmodells für das DLP-Gerät.

Da Projektoren Anzeigegeräte sind, unterstützen sie auch die Umkehrung des Modells, also die Transformation von XYZ zu RGB. Da das Gerätemodell RGB-Raum in XYZ-Raum transformiert, die beide dreidimensional sind, entspricht die Umkehrung dem Lösen von drei nicht linearen Gleichungen in drei unbekannten. Dies kann mit standarden Formellösungstechniken wie Newton-Raphson erfolgen. Es ist jedoch vorzuziehen, zuerst XYZ in Luv zu konvertieren und dann die Luv-Zu-RGB-Transformation um zu konvertieren, da der Luv-Raum besser wahrnehmbar linear als der XYZ-Raum ist.

### <a name="icc-device-model-baseline"></a>BASELINE des GERÄTEMODELLS

Die Workflowinteroperabilität mit VORZGE wird aktiviert, indem ein spezielles Gerätemodellprofil für die BASISGERÄTE-Basislinie erstellt wird, das das Profilobjekt speichert und mithilfe eines xyz-Profils ohne Op eine TRANSFORM-Transformation erstellt. Diese Transformation wird dann verwendet, um zwischen Geräte- und CIEXYZ-Farben zu übersetzen.

![Diagramm, das die C I T E I C C-Workflowinteroperabilität zeigt.](images/cdmp-image168.png)

**Abbildung 10:** Interoperabilität des FOLGENDEN WORKFLOWS

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Konzepte der Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[Windows Color System: Schemas und Algorithmen](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





