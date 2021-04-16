---
title: 'WCS-Farbgerätemodell: Profilschema und Algorithmen'
description: 'Dieses Thema enthält Informationen zum WCS-Farb Gerätemodell-Profil Schema und den zugehörigen Algorithmen. Dieses Thema enthält die folgenden Abschnitte: overviewcolor Device Model Profile Architecture the CDMP schemawcs CDMP v 2.0 Kalibrierung additionthe CDMP Schema elementscolordevicemodelprofilecolordevicemodelnamespaceversionversiondocumentationcrtdevice elementlcddevice elementprojector Device elementscannerdevice elementcameradevice elementrgbprinterdevice elementcmykprinterdevice elementrgbvirtualdevice elementplugindevicetypergbvirtualmessbare rementtypegammatypetgammaoffsetgaintypegammaoffsettypelineargaintypetoneresponsecurvestypeer gamutboundarysamplestypskatpairren listcmykprinterbedinrementtypergbprinterbedinrementtypergbcapturebedinrementtypeonebasedindexrgbprojectorbedinrementtypedisplaybedinrementty Peer Mess rementconditionstypgeometrytypergbprimariesgroupnonnegativecmyksampletybatonnegativergbsampletybatonnegativecmyktybatonnegativergbtypeextensiontybatonnegativexyztypexyztypeder CDMP-Baseline algorithmscrt Gerätemodell baselinelcd Gerätemodell baselinergb Drucker Gerätemodell baselinergb virtuelles Gerätemodell baselinecmyk Drucker Gerätemodell baselinergb Projektor Gerätemodell baselineicc Gerätemodell baselinerelated Topics'
ms.assetid: bbb3b50d-75fc-476d-a011-af7dcc2ac520
keywords:
- Windows Color System (WCS), Color Device Model Profile (CDMP)
- WCS (Windows Color System), Color Device Model Profile (CDMP)
- Bild Farbverwaltung, Color Device Model Profile (CDMP)
- Farbverwaltung, Farb Gerätemodell Profil (CDMP)
- Farben, Farb Gerätemodell Profil (CDMP)
- Windows Color System (WCS), profile
- WCS (Windows Color System), profile
- Bildfarben Verwaltung, profile
- Farbverwaltung, profile
- Farben, profile
- Schemas, Color Device Model Profile (CDMP)
- Algorithmen, Farb Gerätemodell Profil (CDMP)
- Color Device Model Profile (CDMP)
- CDMP (Color Device Model Profile)
- WCS Color-Gerätemodell Profil
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b671bf97625b00c99060e65be4d39c44e5b35f
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104553343"
---
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a>WCS-Farbgerätemodell: Profilschema und Algorithmen

Dieses Thema enthält Informationen zum WCS-Farb Gerätemodell-Profil Schema und den zugehörigen Algorithmen.

Dieses Thema enthält folgende Abschnitte:

-   [Übersicht](#overview)
-   [Architektur des Farb Gerätemodell Profils](#color-device-model-profile-architecture)
-   [Das CDMP-Schema](#the-cdmp-schema)
-   [WCS CDMP v 2.0-Kalibrierungs Addition](#wcs-cdmp-v20-calibration-addition)
-   [Die CDMP-Schema Elemente](#the-cdmp-schema-elements)
    -   [Colordevicemodelprofile](#colordevicemodelprofile)
    -   [Colordevicemodel](#colordevicemodelprofile)
    -   [Namespaceversion](#namespaceversion)
    -   [Version](#namespaceversion)
    -   [Dokumentation](#documentation)
    -   [Crtdevice-Element](#crtdevice-element)
    -   [Lcddevice-Element](#lcddevice-element)
    -   [Projector Device-Element](#projectordevice-element)
    -   [Scannerdevice-Element](#scannerdevice-element)
    -   [Cameradevice-Element](#cameradevice-element)
    -   [Rgbprinterdevice-Element](#rgbprinterdevice-element)
    -   [Cmykprinterdevice-Element](#cmykprinterdevice-element)
    -   [Rgbvirtualdevice-Element](#rgbvirtualdevice-element)
    -   [Pluginde vicetype](#plugindevicetype)
    -   [Rgbvirtualmessrementtype](#rgbvirtualmeasurementtype)
    -   [Gammatype](#gammatype)
    -   [Gammaoffsetgaintype](#gammaoffsetgaintype)
    -   [Gammaoffsetgainlineargaintype](#gammaoffsetgainlineargaintype)
    -   [Toneresponsecurvestype](#toneresponsecurvestype)
    -   [Gamutboundarysamplestype](#gamutboundarysamplestype)
    -   [Floatpaarlist](#floatpairlist)
    -   [Cmykprintermessbare rementtype](#cmykprintermeasurementtype)
    -   [Rgbprintermessbare rementtype](#rgbprintermeasurementtype)
    -   [Rgbcapturemessrementtype](#rgbcapturemeasurementtype)
    -   [Onebasedindex](#onebasedindex)
    -   [Rgbprojector messrementtype](#rgbprojectormeasurementtype)
    -   [Displaymessrementtype](#displaymeasurementtype)
    -   [Messrementconditionstype](#measurementconditionstype)
    -   [Geometrytype](#geometrytype)
    -   [Rgbprimariesgroup](#rgbprimariesgroup)
    -   [Nonnegativecmyksampletype](#nonnegativecmyksampletype)
    -   [Nonnegativergbsampletype](#nonnegativergbsampletype)
    -   [Nonnegativecmyktype](#nonnegativecmyktype)
    -   [Nonnegativergbtype](#nonnegativergbtype)
    -   [ExtensionType](#extensiontype)
    -   [Nonnegativexyztype](#nonnegativexyztype)
    -   [Xyztype](#nonnegativexyztype)
-   [Die CDMP-baselinealgorithmen](#the-cdmp-baseline-algorithms)
    -   [CRT-Gerätemodell-Baseline](#crt-device-model-baseline)
    -   [Baseline für das LCD-Gerätemodell](#lcd-device-model-baseline)
    -   [Basislinie des RGB-Drucker Geräte Modells](#rgb-printer-device-model-baseline)
    -   [Grundlegende Konfiguration des virtuellen Geräte Modells](#rgb-virtual-device-model-baseline)
    -   [Baseline des CMYK-Drucker Geräte Modells](#cmyk-printer-device-model-baseline)
    -   [Basislinie des RGB-projektorgeräts](#rgb-projector-device-model-baseline)
    -   [Basislinie des Modells für das Modell](#icc-device-model-baseline)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Dieses Schema wird verwendet, um den Inhalt eines Farb Gerätemodell Profils (CDMP) anzugeben. Die zugeordneten Basis Linien Algorithmen werden nachfolgend beschrieben.

Das grundlegende Gerätemodell Profil-Schema (DMP) besteht aus den Stichproben Messungs Daten.

Die Stichproben Komponente des DMP-XML-Schemas bietet Unterstützung für grundlegende farbmessungs Ziele und konzentriert sich auf allgemeine Standard Ziele und Ziele, die für die Basisgeräte Modelle optimiert sind.

Darüber hinaus stellt das Geräte Profil spezifische Informationen zum Zielgeräte Modell bereit und stellt eine Richtlinie bereit, die vom baselinefallback-Gerätemodell verwendet werden kann, wenn das Zielmodell nicht verfügbar ist. Die Profil Instanzen können private Erweiterungen mit XML-Standard Erweiterungs Mechanismen enthalten.

## <a name="color-device-model-profile-architecture"></a>Architektur des Farb Gerätemodell Profils

![Diagramm, in dem die Informationen angezeigt werden, die ein Gerätemodell Profil bilden.](images/cdmp-image002new.png)

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



## <a name="wcs-cdmp-v20-calibration-addition"></a>WCS CDMP v 2.0-Kalibrierungs Addition

Das **colordevicemodel** -Element des CDMP-Schemas wurde in Windows 7 aktualisiert, um das neue Kalibrierungs Element einzuschließen. Das folgende Beispiel zeigt die Änderung des CDMP-Schemas.


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



## <a name="the-cdmp-schema-elements"></a>Die CDMP-Schema Elemente

> [!Note]  
> Primäre Samplings sind primär Beispiele von rot, grün, blau, schwarz und weiß. Eine primäre Anlauf Linie ist eine klangliche Abweichung von der geringsten Helligkeit bis zum vollständigen primär Wert. Die maximale Anzahl von Einträgen in einer tonampe beträgt 4096.

 

> [!Note]  
> Für DMPs sind Messungs Daten erforderlich.

 

### <a name="colordevicemodelprofile"></a>Colordevicemodelprofile

Dieses Element weist den Typ colordevicemodel auf.

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

### <a name="colordevicemodel"></a>Colordevicemodel

Dieses Element stellt eine Sequenz der folgenden unter Elemente dar.

1.  Profilnamen Zeichenfolge,
2.  optionale Beschreibungs Zeichenfolge,
3.  optionale Autor Zeichenfolge,
4.  optionale "bedinrementconditions", "bedinrementconditionstype",
5.  Self-Luminous boolescher Wert,
6.  Maxcolorant float,
7.  Mincolorant float,
8.  Auswahl von Elementen
    1.  Crtdevice,
    2.  Lcddevice,
    3.  Rgbprojector Device,
    4.  Scannerdevice,
    5.  Cameradevice,
    6.  Rgbprinterdevice,
    7.  Cmykprinterdevice,
    8.  Rgbvirtualdevice,
9.  Plugindevice,
10. Optionaler Erweiterungstyp für Erweiterungen

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft. Zeichen folgen-unter Elemente können maximal 10.000 Zeichen enthalten. Das maxcolorant-Unterelement muss größer oder gleich 0 (null) und größer als das mincolorant-Unterelement sein. Mincolorant kann negativ sein.

### <a name="namespaceversion"></a>Namespaceversion

xmlns: CDM = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

### <a name="version"></a>Version

Version = "1,0" mit Windows Vista.

Überprüfungs **Bedingungen:** Jeder Versions Wert &gt; 0,1 oder &lt; = 2,0 ist gültig, um nicht unterbrechende Änderungen im Format zu unterstützen.

### <a name="documentation"></a>Dokumentation

Gerätemodell Profil-Schema.

Copyright (C) Microsoft. Alle Rechte vorbehalten.

### <a name="crtdevice-element"></a>Crtdevice-Element

Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines ".

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

### <a name="lcddevice-element"></a>Lcddevice-Element

Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines ".

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

### <a name="projectordevice-element"></a>Projector Device-Element

Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines "festgelegten" "" "" "".

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

### <a name="scannerdevice-element"></a>Scannerdevice-Element

Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines "festgelegten"-rgbcapturemessrementtype.

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

### <a name="cameradevice-element"></a>Cameradevice-Element

Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines "festgelegten"-rgbcapturemessrementtype.

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

### <a name="rgbprinterdevice-element"></a>Rgbprinterdevice-Element

Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines "festgelegten rgbprintermessrementtype".

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

### <a name="cmykprinterdevice-element"></a>Cmykprinterdevice-Element

Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines festgelegten Elements "".

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

### <a name="rgbvirtualdevice-element"></a>Rgbvirtualdevice-Element

Dieses Element ist eine Sequenz von unter Elementen eines rgbvirtualmessrementdatatype.

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

### <a name="plugindevicetype"></a>Pluginde vicetype

Bei diesem Element handelt es sich um eine Sequenz eines GUID-guidtype und aller untergeordneten Elemente.

Überprüfungs **Bedingungen:** Die GUID wird verwendet, um die GUID der DM-Plug-in-dll zuzuordnen. Es sind maximal 100.000 benutzerdefinierte unter Elemente vorhanden.

### <a name="rgbvirtualmeasurementtype"></a>Rgbvirtualmessrementtype

Dieses Element ist eine Sequenz, die aus

1.  Rgbprimariesgroup-Gruppe
2.  Eine Auswahl von
3.  -   Gamma
    -   Gammaoffsetgewinn
    -   Gammaoffsetgainlineargam
    -   Toneresponsecurves-Elemente

4.  optionale gamutboundarysamples gamutboundarysamplestype
5.  Timestamp-DateTime

Überprüfungs **Bedingungen:** Jedes untergeordnete Element dieser Typen verfügt über eigene Überprüfungs Bedingungen.

### <a name="gammatype"></a>Gammatype

Dieses Element ist ein komplexer Typ, der aus dem-Attribut besteht.

-   Gamma nonnegativefloattype

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="gammaoffsetgaintype"></a>Gammaoffsetgaintype

Dieses Element ist ein komplexer Typ, der aus den Attributen besteht.

-   Gamma nonnegativefloattype
-   Offset nonnegativefloattype
-   Nonnegativefloattype gewinnen

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="gammaoffsetgainlineargaintype"></a>Gammaoffsetgainlineargaintype

Dieses Element ist ein komplexer Typ, der aus den Attributen besteht.

-   Gamma nonnegativefloattype
-   Offset nonnegativefloattype
-   Nonnegativefloattype gewinnen
-   Linear Gewinn nonnegativefloattype
-   Transitionpoint nonnegativefloattype.

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="toneresponsecurvestype"></a>Toneresponsecurvestype

Dieses Element ist eine Sequenz von

1.  Redtrc floatpaarlist
2.  Greentrc floatpaarlist
3.  Bluetrc floatpaarlist

Das-Element verfügt auch über ein Attribut vom Typ "unsignetdint".

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="gamutboundarysamplestype"></a>Gamutboundarysamplestype

Dieses Element ist eine Sequenz von RGB rgbtypes.

Überprüfungs **Bedingungen:** Derzeit unbegrenzte Anzahl von vorkommen, die auf der Grundlage des Branchen Feedbacks begrenzt werden.

### <a name="floatpairlist"></a>Floatpaarlist

Dieses Element ist ein einfacher Typ von Gleit Komma Zahlen.

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="cmykprintermeasurementtype"></a>Cmykprintermessbare rementtype

Dieses Element ist ein

1. die Sequenz des colorcube-Elements, das aus einer Sequenz von Sample nonnegativecmyksampletype besteht.

2. Timestamp-DateTime-Attribut.

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="rgbprintermeasurementtype"></a>Rgbprintermessbare rementtype

Dieses Element ist ein

1. die Sequenz des colorcube-Elements, das aus einer Sequenz von Sample nonnegativergbsampletype besteht.

2. Timestamp-DateTime-Attribut.

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="rgbcapturemeasurementtype"></a>Rgbcapturemessrementtype

Dieses Element ist eine Sequenz von

1.  ComplexType für primaryindex von
2.  1.  Weiß onebasedindex
    2.  Optionaler schwarzer onebasedindex
    3.  Optionaler roter onebasedindex
    4.  Optionales grünes onebasedindex
    5.  Optionaler blauer onebasedindex
    6.  Optionales Cyan onebasedindex
    7.  Optionaler onebasedindex (optional)
    8.  Optionaler gelber onebasedindex

3.  Neutralindizes von Linien von onebasedindex
4.  Colorsamples-Sequenz von Sample nonnegativergbsampletype

Das-Element verfügt auch über ein Timestamp-DateTime-Attribut.

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="onebasedindex"></a>Onebasedindex

Dieses Element ist eine einfache Art von Einschränkungs Basis ohne Vorzeichen (int) mit minInclusive Value = "1".

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="rgbprojectormeasurementtype"></a>Rgbprojector messrementtype

Dieses Element ist eine Sequenz von

1.  Rgbprimariesgroup-Gruppe
2.  Color Samples-Element, das aus einer Sequenz von Sample nonnegativergbsampletype besteht

Das-Element verfügt auch über ein Timestamp-DateTime-Attribut.

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="displaymeasurementtype"></a>Displaymessrementtype

Dieses Element ist eine Sequenz von

1.  Gruppe "rgbprimariesgroup"
2.  Grayramp der Sequenz von Sample nonnegativergbtype
3.  Redramp der Sequenz von Sample nonnegativergbtype
4.  Greenramp der Sequenz von Sample nonnegativergbtype
5.  Blueramp der Sequenz von Sample nonnegativergbtype

Das displaymessrementtype-Element weist auch ein Timestamp-DateTime-Attribut auf.

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="measurementconditionstype"></a>Messrementconditionstype

Der Wert für "bedinrementconditionstype" ist eine Sequenz von unter Elementen, die Folgendes enthält:

1.  Zeichen folgen-Enumerationswert "CIEXYZ" für colorspace-Einschränkung
2.  optionale Auswahl von "White Point nonnegativexyztype" oder "whitepointname String Enumeration of values, D65, A" oder F2
3.  Geometry-geometrytype
4.  Aperturesize Integer in Millimeter

Standardwerte:

1.  RGB-und CMYK-Drucker:
    1.  CIEXYZ-messrementspacetype
    2.  D50-whitepointvalue
    3.  0/45 geometrytype
    4.  10mm-aperturesize
2.  Can
    1.  CIEXYZ-messrementspacetype
    2.  D50-whitepointvalue
    3.  0/45 geometrytype
    4.  10mm-aperturesize
3.  Zeigt ein virtuelles Gerät an:
    1.  CIEXYZ-messrementspacetype
    2.  D65-whitepointvalue
    3.  0/45 geometrytype
    4.  10mm-aperturesize
4.  Blitzer
    1.  CIEXYZ-messrementspacetype
    2.  D65-whitepointvalue
    3.  Direkter geometrytype
    4.  10mm-aperturesize

Überprüfungs **Bedingungen:** Die Validierung jedes untergeordneten Elements wird durch Validierungs Bedingungen für diese unter Elemente bestimmt. Wenn ein untergeordnetes Element fehlt, wird der jeweilige Standardwert für den Geräte Modelltyp verwendet.

### <a name="geometrytype"></a>Geometrytype

String

Enumerationswerte:

-   "0/45"
-   "0/diffus"
-   "Diffuses/0"
-   Unmittelbaren

Überprüfungs **Bedingungen:** Jeder Wert außer den aufgelisteten Enumerationswerten ist ungültig. Diese Informationen ändern das Baseline-Verarbeitungs Verhalten nicht.

### <a name="rgbprimariesgroup"></a>Rgbprimariesgroup

Dieses Element ist eine Sequenz von

1.  Whiteprimary nonnegativexyztype
2.  Redprimary nonnegativexyztype
3.  Greenprimary nonnegativexyztype
4.  Blueprimary nonnegativexyztype
5.  Blackprimary nonnegativexyztype

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="nonnegativecmyksampletype"></a>Nonnegativecmyksampletype

Dieses Element ist eine Sequenz von

1.  CMYK nonnegativecmyktype
2.  CIEXYZ nonnegativexyztype

Das Element verfügt auch über eine optionale attributtagzeichenfolge.

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="nonnegativergbsampletype"></a>Nonnegativergbsampletype

Dieses Element ist eine Sequenz von

1.  RGB nonnegativergbtype
2.  CIEXYZ nonnegativexyztype

Das Element verfügt auch über eine optionale attributtagzeichenfolge.

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="nonnegativecmyktype"></a>Nonnegativecmyktype

Dieses Element, das aus Attributen besteht.

1.  C float
2.  M float
3.  Y float
4.  K float

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="nonnegativergbtype"></a>Nonnegativergbtype

Dieses Element, das aus Attributen besteht.

1.  R float
2.  G float
3.  B float

Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.

### <a name="extensiontype"></a>ExtensionType

Das ExtensionType-Element ist eine Sequenz eines beliebigen untergeordneten Elementtyps und wird für proprietäre Informationen von nicht-Microsoft-Anwendungen verwendet.

Überprüfungs **Bedingungen:** Dieses Element ist optional. Es können maximal 1000 Erweiterungs unter Elemente vorhanden sein.

### <a name="nonnegativexyztype"></a>Nonnegativexyztype

Das nonnegativexyztype-Element besteht aus nonnegativefloattype mit drei IEEE-Gleit Komma Elementen mit einfacher Genauigkeit namens "X", "Y" und "Z". Diese Werte sind auf die Maßwerte der DMP-profile beschränkt. Bei diesen Messungen kann es sich entweder um absolute (nicht relative) CIEXYZ 1931-reflektierte Werte oder absolute (nicht relative) CIEXYZ 1931 Direct-Werte (Transmissive) in den quadratischen Einheiten von Kerzen pro Meter handelt.

Überprüfungs **Bedingungen:** Nur reale Werte sind gültig, und negative CIEXYZ-Mess Werte sind ungültig. Da es sich hierbei um absolute Werte handelt, können Werte größer als 1,0 f sein. Ein angemessener Grenzwert für "X", "Y" oder "Z". der Wert ist willkürlich auf 10000.0 f festgelegt.

### <a name="xyztype"></a>Xyztype

Das xyztype-Element besteht aus drei IEEE-Gleit Komma Werten mit einfacher Genauigkeit: "X", "Y" und "Z".

## <a name="the-cdmp-baseline-algorithms"></a>Die CDMP-baselinealgorithmen

### <a name="crt-device-model-baseline"></a>CRT-Gerätemodell-Baseline

Um dieses Modell zu verstehen, müssen Sie sowohl den Charakterisierungs Prozess als auch die Geräte Modellierung in Erwägung gezogen. Im Charakterisierungs Prozess werden XYZ-Messungen zuerst für die Farben ausgeführt, die durch Ausfüllen des Anzeige Puffers eines CRT-Anzeige Geräts abgerufen werden. In den folgenden Beispiel Werten werden gute Daten für das CRT-Basisgeräte Modell generiert:

Rot: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Grün: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blau: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutrals: R = G = B = 0, 8, 16, 32, 64, 128, 192, 255

Andere Inkremente als 15 und nichtlineare Inkremente können ebenfalls verwendet werden. Alle roten, grünen, blauen und neutralen Rampen müssen mindestens drei Stichproben enthalten, es wird jedoch empfohlen, weitere Beispiele zu erhalten. Sie müssen Beispiele für pure rot, grün, blau, schwarz und weiß bereitstellen. Die Beispiele müssen nicht gleichmäßig verteilt werden.

Der Prozess der buildstimulmatrizen besteht aus zwei Schritten. Schätzen Sie zuerst den Wert von "Black Point XYZ" oder "FLARE". Dieser Schritt basiert größtenteils auf der Arbeit von Berns \[ 3 \] mit einer leicht geänderten Zielfunktion für die nichtlineare Optimierung. Zweitens berechnen Sie die Matrix für die Auswert Erstellung basierend auf dem Ergebnis aus Schritt 1 und auch aus einer durchschnittlichen Berechnung für alle pro-Channel-Messungen, nicht nur für die maximale digitale Anzahl.

Jeder dieser Schritte enthält ausführliche Prozeduren. Der Ausgangspunkt ist die Rampen (17 Schritte in unserem Beispiel) für jeden R-, G-und B-Kanal. Wenn die XYZ-Messungen auf der Chromaticity- *XY* -Ebene dargestellt werden, ist in Abbildung 1 eine typische Situation dargestellt. In Schritt 1 wird ein Problem mit der nichtlinearen Optimierung gelöst, um den am besten geeigneten schwarzen Punkt zu finden, der die Abweichung in der Chromaticity als eine durchläuft, die auf den Kanälen R, G und B verläuft. Basierend auf Berns \[ 3 \] wird ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>K</sub>* ) gesucht, die die folgende Zielfunktion minimiert:

![Zeigt die Zielfunktion an, bei der SR, SG und SB der Satz von Datenpunkten in den Kanälen R, G und B entsprechen.](images/cdmp-formula1.png)

Dabei sind *s <sub>R</sub>*,*s <sub>G</sub>* und *s <sub>B</sub>* der Satz von Datenpunkten, die den Punkten in den Kanälen R, G und b entsprechen. Definieren Sie für alle festgelegten *e* Folgendes:

![Zeigt eine Formel zum Definieren von festgelegten S an.](images/cdmp-formula2.png)

In der vorangehenden \|  \| ist s die Kardinalität von *s*, d. h. die Anzahl der Punkte in den festgelegten *s*. ![ Zeigt eine Formel für die Chromatizität eines Punkts an.](images/cdmp-formula3.png) Gibt an, dass die Chromaticity-Koordinaten des Punkts ![ eine formaula für einen Punkt anzeigt.](images/cdmp-formula4.png) , ![ zeigt eine Formel für den Mittelwert oder Mittelpunkt der Masse ](images/cdmp-formula5.png) an., ist der Durchschnitt oder Mittelpunkt der Masse aller Punkte in den festgelegten *S* auf der Ebene der Chromaticity. Folglich ![ zeigt eine Formel für die Summe eines zweiten Zeitpunkts von Punkten an.](images/cdmp-formula6.png) ist die Summe aus den zweiten Augenblicken in Bezug auf den Mittelpunkt der Masse und ist ein Maß dafür, wie die Punkte verteilt werden. Schließlich wird ![ eine Formel für das Gesamt Measure der Verteilung von drei Clustern von Punkten angezeigt.](images/cdmp-formula7.png) ist ein Gesamt Measure der Verteilung der drei Cluster Punkte auf die jeweiligen Mittelpunkte.

In der Berechnung von wird ![ eine Formel von f (X, Y, Z;) angezeigt. XK, YK, ZK).](images/cdmp-formula8.png) Wenn ![ eine Formel für X. anzeigt ](images/cdmp-formula9.png) , wird die Berechnung übersprungen und die Kardinalität von *S* entsprechend angepasst.

Trotz der offensichtlichen Komplexität der Zielfunktion handelt es sich um eine Summe der Quadrate von vielen differenzierbaren Funktionen in *X <sub>K</sub>*,*Y <sub>k</sub>Z <sub>k</sub>* (17 Punkte 2 *XY* -Components 3 Channels = 102, im Beispiel) und ist daher für Standardverfahren für nichtlineare minimal Quadrate geeignet, wie z. b. den Levenberg-Marquardt Algorithmus, bei dem es sich um den in WCS verwendeten Algorithmus handelt. Beachten Sie, dass sich die vorangehende Zielfunktion von der in Berns 3 vorgeschlagenen unterscheidet, \[ \] dass die letztere Funktion die Varianz der Entfernungen vom Mittelpunkt der Masse misst, sodass die Varianz NULL ist, wenn die Punkte vom Mittelpunkt der Masse entfernt sind, auch wenn Sie vielleicht etwas darüber verteilt sind. Im Beispiel wird die Verteilung von Punkten direkt mit den zweiten Augenblicken gesteuert.

Wie bei jedem iterativen Algorithmus für das Problem bei nichtlinearen Quadraten erfordert Levenberg-Marquardt eine anfängliche Vermutung. Es gibt zwei offensichtliche Kandidaten. Eins ist (0,0); der andere ist der gemessene schwarze Punkt. Für den allgemeinen Tabellen Ausdruck wird der gemessene schwarze Punkt zuerst als erste Vermutung verwendet. Wenn maximal 100 Iterationen überschritten werden, ohne dass ein Schwellenwert mit einer durchschnittlichen Entfernung von 0,001 der einzelnen Punkte von der Mitte der Masse erreicht wird (was einem Schwellenwert von (0,001) 17 3 = 0,000051 für die Zielfunktion entspricht), wird eine andere Runde von Iterationen mit der anfänglichen Vermutung (0, 0, 0) ausgeführt. Die resultierende Schätzung des schwarzen Punkts ist XYZ, verglichen mit der besten Schätzung aus der vorherigen Runde der Iterationen (mit dem gemessenen schwarzen Punkt als anfängliche Vermutung). Verwenden Sie die Schätzung, die den kleinsten Wert für die Zielfunktion liefert. Die Auswahl von 100 Iterationen und der Fehler Entfernung von 0,001 wurde jeweils empirisch ausgewählt. In zukünftigen Versionen kann es sinnvoll sein, die Fehler Entfernung zu parametrisieren.

Das Ergebnis von Schritt 1 ist der geschätzte schwarze Punkt ( *X <sub>k</sub>*,*Y <sub>K</sub>*,*Z <sub>k</sub>* ). In Schritt 2 wird die Matrix mit den drei Stufen ermittelt, indem die Chromatizität der Punkte in den drei in Schritt 1 erhaltenen Clustern überschritten wird. Bei CRTs erfolgt dies in erster Linie, um die Auswirkungen von Messfehlern zu minimieren. Die Punkte, die bei der Durchschnittsberechnung der Chromatizität verwendet werden, müssen die gleichen Punkte sein, die bei der Optimierung in Schritt 1 verwendet werden Anders ausgedrückt: Wenn der erste Punkt (digitale Anzahl 15 im Beispiel) in jeder Rampe im Optimierungs Schritt verworfen wird, muss das gleiche im Mittelwert durchgeführt werden. , Wenn ![ Formeln der durchschnittlichen Chromatizität für Koordinaten in den roten und grünen Kanälen anzeigt.](images/cdmp-formula10.png) und ![ zeigt eine Formel für den Mittelwert der-Koordinaten im blauen Kanal an.](images/cdmp-formula11.png) Die Mittelwert Koordinaten der roten, grünen und blauen Kanäle werden im Mittelwert der folgenden Prozedur festgelegt. Lösen Sie zunächst das lineare 3? 3-System:

![Zeigt den ersten Teil des Verfahrens zum Lösen eines linearen 3? 3-Systems.](images/cdmp-formula12.png)

![Zeigt den zweiten Teil des linearen Systems 3? 3 an.](images/cdmp-formula13.gif)![Zeigen Sie den t-index "t" am Ende des zweiten Teils des linearen Systems 3? 3 an.](images/cdmp-formula14.gif)

*X <sub>w</sub>*,*Y <sub>w</sub>*,*Z <sub>W</sub>*

![Zeigt den letzten Teil des Verfahrens zum Lösen eines linearen 3? 3-Systems.](images/cdmp-formula15.png)

Nachdem die matrixaus der Matrix festgelegt wurde, folgt die Bestimmung von Tonkurven dem Standardansatz. Bei CRT-Anzeige wird davon ausgegangen, dass die einzelnen Kanäle dem "Gog"-Modell folgen:

![Zeigt die Formel für das ' g O g '-Modell an.](images/cdmp-formula16.png)

Dabei steht *k <sub>g</sub>* für den "Gewinn", 1-*k <sub>g</sub>* für den "Offset" und? ist das "Gamma". Die umgekehrte Matrix der Matrix mit den drei Werten wird auf die XYZ-Daten der neutrale angewendet, um die linearen RGB-Daten abzurufen, die dann mit den digitalen RGB-Werten korreliert werden, indem eine nichtlineare Regression für das Gog-Modell verwendet wird. Diese Merkmale müssen nicht für die R-, G-und B-Kanäle identisch sein und sind im Allgemeinen nicht identisch.

Berns \[ 1 \] : Berns, *Abrechnungs-und Saltzman-Prinzipien der Farb Technologie*, 3 <sub>.</sub> d. John Wiley & Sons (2000).

Berns \[ 2 \] : Berns und Katoh, die digitale zu radiometrische Übertragungsfunktion für computergesteuerte CRT-Anzeige, das *Cie-Expertensymposium "97 Color Standards for Imaging Technology*, Nov. 1997.

Berns \[ 3 \] : Berns, Fernandez und Taplin, schätzen der Black-Level Computer-Controlled anzeigen, *Farb Recherche und Anwendung*, 28:379-383 Wiley-Zeitschriften, Inc. (2003)

Kang \[ 1 \] : Kang, *Farb Technologie für elektronische Imaging-Geräte*, spie (1997)

Katoh \[ 1 \] : Katoh, Deguchi und Berns, eine genaue Charakterisierung des CRT-Monitor-Vorschlags (II) für eine Erweiterung der Cie-Methode und deren Verifizierung, *Opt. Rev.* 8:397-408 (2001)

### <a name="lcd-device-model-baseline"></a>Baseline für das LCD-Gerätemodell

Die Basislinie für das LCD-Gerätemodell ähnelt der Basislinie des CRT-Geräte Modells. In diesem Abschnitt wird erläutert, wie sich die LCD-Modellierung von der CRT-Modellierung unterscheidet.

Ein Unterschied besteht darin, dass Sie nicht davon ausgehen können, dass die LCD-Anzeige dem für CRTs verwendeten Gog-Modell folgt und die audiokurven durch Interpolationen der gemessenen Daten abgerufen werden. Aus diesem Grund sollte die Geräte neutrale Achse häufiger getestet werden.

Im folgenden finden Sie einige typische Beispiel Werte, die gute Daten für die Basislinie für das LCD-Gerätemodell generieren können:

Rot: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Grün: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blau: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.

Der Prozess der Mittelwert Messung gemessener Farbwerte zum Abrufen der chromatitäten für die Geräte Replikate ist für LCDs kritischer als bei CRTs. Wenn XYZ-Messungen auf der Chromaticity- *XY* -Ebene dargestellt werden, ist in Abbildung 1 eine typische Situation dargestellt. Beachten Sie, dass sich die Chromaticity auf den schwarzen Punkt bewegt. Dies liegt daran, dass alle LCDs über eine bestimmte Menge an leichten Lecks verfügen.

![Diagramm, das ein Diagramm der Chromatizität anzeigt, in dem Rohdaten ohne Korrektur verwendet werden.](images/cdmp-lcd-dmp-figure1.png)

**Abbildung 1** : das Chromaticity-Diagramm mit Rohdaten ohne Korrektur

Wenn dies von den RAW-XYZ-Messungen subtrahiert wird, wird eine typische Situation in Abbildung 2 dargestellt. Die Punkte sind nun auf drei Mittelpunkte gruppiert, auch wenn Sie nicht identisch sind. Der für CRTs beschriebene Durchschnitts Prozess verbessert die Ergebnisse für LCDs erheblich.

![Diagramm, das ein Diagramm der Chromatizität anzeigt, das Rohdaten mit einem angepassten schwarzen Punkt verwendet.](images/cdmp-lcd-dmp-figure2.png)

**Abbildung 2** : das Chromaticity-Diagramm mit Daten mit angepasstem Schwarzpunkt

### <a name="rgb-capture-device-model-baseline"></a>RGB-Gerätemodell-Baseline erfassen

Das Basis Linien-RGB-Erfassungsgeräte Modell ist eine Unterklasse der idevicemodel-Klasse. In der farbige Metrik-Charakterisierung von Farb Erfassungs Geräten, wie z. b. Scanner und Digitalkameras, wird die folgende Vorgehensweise verwendet. Ein Ziel, das aus farbpatches mit bekannten CIEXYZ-Werten besteht, wird mit dem Erfassungsgerät erfasst. Das Ergebnis der Erfassung ist ein RGB-Bitmap-Bild, in dem die Farbe der einzelnen Patches in einem RGB-Wert codiert ist. Diese Geräte RGB-Werte sind für ein bestimmtes Erfassungsgerät spezifisch. Das Ziel der farbige Metrik-Charakterisierung besteht darin, eine empirische Beziehung zwischen den RGB-Werten des Geräts und den CIEXYZ-Werten herzustellen, oder eine mathematische Transformation zwischen RGB und XYZ, die das Verhalten des Aufzeichnungs Geräts so genau wie möglich modelliert.

Eine solche mathematische Transformation kann in gewissem Maße durch Polynomen von niedrigem Grad modelliert werden. Dieses Verfahren wird in der-Literatur ausführlich erläutert, z \[ . b. Kang 92 \] , Kang \[ 97 \] . In Kang \[ 97 \] wird ein Ansatz berichtet, der einen Satz von drei polynomials mit 3, 6, 8, 9, 11, 14 oder 20 Begriffen in den Variablen R, G und B verwendet, während die drei Polynomen jeweils in die X-, Y-und Z-Komponenten des CIEXYZ-Raums fallen. Für das 20-Term-polynomal lautet das Formular:

![Zeigt die 20-Term polynomal an.](images/cdmp-formula20.png)

Es gibt ähnliche Ausdrücke für Y und Z. Das mathematische Verfahren für die Anpassung der Polynomen liegt innerhalb der "multivariate Linear Regression" und wird in jedem elementaren Text in der Statistik beschrieben.

Bei dieser Methode der linearen Regression wird die "Right"-Zielfunktion nicht minimiert. Entwurfs bedingt findet die lineare Regression die kleinste Quadrats Lösung. Dies impliziert, dass die erhaltenen Koeffizienten die Gesamtsumme der Quadrate von Fehlern im zugrunde liegenden Raum oder die Summe der Quadrate der euklidischen Entfernungen minimieren. In der Praxis möchten Sie die Summe der Quadrate von minimieren? Es, wo? E ist einer der akzeptierten Standards, z. b. CIE94. Das minimieren dieser Zielfunktion ist ein nichtlineares Regressions Problem.

In der neuen Engine ist Lab bis XYZ der CIE-Farbraum, der in zurückgezogen wird. das 20-jährige kubische polynomal wird als Modell für das Erfassungsgerät oder Koeffizienten ls, wie z. b., verwendet, so dass die folgenden Polynomen die Summe der Quadrate von minimieren? E <sub>CIE94</sub> s.

![Zeigt eine Reihe von polynomialen Formeln an.](images/cdmp-formula21.png)

Die Lösung ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) im 60 dimensionalen echten numerischen Bereich **R** 203 muss so lauten, dass der folgende Gesamtfehler minimiert wird:

![Zeigt den Gesamtfehler an, der minimiert werden soll.](images/cdmp-formula22.png)

wobei die sumzierung über alle Datenpunkt Paare erfolgt (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*).*L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* ) im DataSet mit Stichproben und zusätzliche Steuerungs Punkte, die in den folgenden Bereichen ausführlich erläutert werden. Dies ist ein nichtlineares Regressions Problem, weil die Parameter *?<sub> i</sub>*, *a <sub>i</sub>*, * <sub>i</sub>* Eingabe in die Zielfunktion auf nichtlineare Weise (nicht quadratisch).

Da die Zielfunktion? ist eine nichtlineare (und nicht quadratische) Funktion der Parameter *?<sub> i</sub>*, *a <sub>i</sub>* und * <sub>i</sub>*, Sie müssen auf iterative Techniken zurückgreifen, um das Optimierungsproblem zu lösen. Da es sich bei der Form der Zielfunktion um eine Summe von Quadraten handelt, wird eine standardmäßige Optimierungstechnik verwendet, die als Levenberg-Marquardt-Algorithmus bezeichnet wird. Es wird als Methode der Wahl für nichtlineare, kleinste Quadrate behandelt. Für iterative Algorithmen, wie z. b. Levenberg-Marquardt, müssen Sie eine anfängliche Vermutung angeben. Ein guter ursprünglicher Schätzwert ist normalerweise wichtig, um den richtigen Minimalwert zu ermitteln. In diesem Fall ist ein guter Kandidat für die anfängliche Schätzung die Lösung des linearen Regressions Problems. Minimieren Sie zunächst die Summe des Quadrats von euklidischen Entfernungen im Lab-Raum, indem Sie eine quadratische Zielfunktion definieren:

![Zeigt eine definierte quadratische Zielfunktion an.](images/cdmp-formula23.png)

Die mathematische Lösung für das Problem "lineare geringste Quadrate" ist bekannt. Denn *?<sub> Ich</sub>* wird nur in der *L* -Modellierung angezeigt, *ein <sub>i</sub>* wird nur in der *u* -Modellierung angezeigt, und * <sub>i</sub>* wird nur in der *v* -Modellierung angezeigt. Das Optimierungsproblem kann in drei Unterprobleme zerlegt werden: eine für *L*, eine für *u* und eine für *v*. Beachten Sie die *L* -Gleichungen. (Die *u* -Gleichungen und die *v* -Gleichungen folgen exakt dem gleichen Argument.) Das Problem der Minimierung der Summe der Fehler Quadrate in *L* kann als das Lösen der folgenden Matrix Gleichung in den geringsten Quadraten ausgedrückt werden:

![Zeigt eine Matrix Gleichung für L an.](images/cdmp-formula24.png)

Dabei steht *N* für die Gesamtanzahl der Datenpunkte (ursprüngliche Stichprobenpunkte Plus Steuerungs Punkte, die wie unten beschrieben erstellt werden). Normalerweise ist *N* viel größer als 20, sodass die vorangehende Gleichung über gestellt wird, sodass eine kleinste Quadrats Lösung erforderlich ist. Eine geschlossene Formular Projekt Mappe für **?** verfügbar:

![Zeigt eine geschlossene Formular Projekt Mappe an.](images/cdmp-formula25.png)

In der Praxis wird die direkte Auswertung mithilfe der geschlossenen Formular Lösung nicht verwendet, da Sie über schlechte numerische Eigenschaften verfügt. Stattdessen wird ein beliebiger matrixfaktorisierungsalgorithmus auf die Koeffizienten-Matrix angewendet, wodurch das System der Gleichungen in eine kanonische Form reduziert wird. In der aktuellen Implementierung wird die einmalige Wert Zerlegung (Single Value Zerlegung, SVD) auf die Matrix **R** angewendet, und dann wird das resultierende, zusammengesetzte System gelöst.

Die Lösung für das lineare Regressions Problem, das von angegeben wird, ![ zeigt die Lösung für das Problem der linearen Regression.](images/cdmp-formula26.png) wird als Ausgangspunkt des Levenberg-Marquardt Algorithmus verwendet. In diesem Algorithmus wird ein Test Schritt berechnet, der den Punkt näher an die optimale Lösung verschieben sollte. Der Test Schritt erfüllt einen Satz linearer Gleichungen, der vom funktionalen Wert und den Werten der Ableitungen am aktuellen Punkt abhängt. Aus diesem Grund sind die Ableitungen der Zielfunktion? in Bezug auf die Parameter *?<sub> Ich</sub>* bin *für <sub></sub> <sub></sub>* den Levenberg-Marquardt Algorithmus Eingaben erforderlich. Obwohl es 60 Parameter gibt, gibt es eine Verknüpfung, mit der Sie viel weniger berechnen können. Nach der Ketten Regel von "Kalkül"

![Zeigt eine Gleichung an, die eine Verknüpfung mithilfe der Ketten Regel von Kalkül zulässt.](images/cdmp-formula27.png)

Dabei ist *j* = 1, 2,, 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* der CIELAB-Wert des *i* Th-Beispiel Punkts, und *R <sub>IJ</sub>* ist der (*i*,*j* ) Th-Eintrag der oben definierten Matrix- **R** . Anstatt also Ableitungen für 60-Parameter zu berechnen, können Sie die Ableitungen für *L*,*a* und *b* mithilfe von numerischer vorwärts Differenzierung berechnen.

Außerdem ist es erforderlich, ein Stopp Kriterium für iterative Algorithmen einzurichten. In der aktuellen Implementierung werden die Iterationen beendet, wenn das mittlere quadratische DECIE94 kleiner als 1 ist, oder wenn die Anzahl der durchgeführten Iterationen 10 überschritten hat. Die Zahl 10 ergibt sich aus der Praxis, dass bei den ersten Iterationen, die den Fehler nicht signifikant verringern, weitere Iterationen nicht viel anderes unterstützen, als den Punkt in einer oszillatorischen Weise zu verschieben, d. h., der Algorithmus wird möglicherweise nicht konvergiert. Auch wenn der Algorithmus abweicht, können wir sicher sein, dass das DECIE94 nicht schlechter ist als das, was wir gestartet haben, d. h. mit den Parametern, die aus der linearen Regression abgerufen wurden.

Selbst bei der vorhergehenden Methode der nichtlinearen Regression gibt es mehrere Probleme bei der Anpassung. Ein Problem besteht darin, dass die Polynomen tendenziell über die Datenpunkte hinausgehen oder diese überschreiten. Künstliche lokale Maximen und Mindestwerte können im Anpassungsprozess eingeführt werden. Dies kann durch die Verwendung von polynomialen mit niedrigem Grad gegenseitig erfolgen. Dies ist der Grund, warum Sie nicht mehr als drei Grad verwenden sollten. Ein schwerwiegenderer Aspekt der Überschreibung oder des Unterlaufs besteht darin, dass ein polynomal theoretisch einen beliebigen realen Wert annehmen kann, da der für die Modellierung verwendete Speicherplatz in der Regel über physische Einschränkungen und praktische Einschränkungen verfügt. CIEXYZ muss alle X, Y, Z nicht negativ aufweisen, eine physische Einschränkung. In der Praxis beanspruchen Sie nur Werte in der Größe von Hunderten, nicht Tausender oder höher. Ebenso hat CIELAB oder CIELUV eigene physische und praktische Einschränkungen. Wenn der RGB-Speicherplatz mit Beispiel Punkten ausreichend gefüllt ist, ist das Problem des über Schießens oder Unterlaufs nicht schwerwiegend. Die erfassten RGB-Punkte vom Erfassungsgerät füllen den RGB-Speicherplatz jedoch in der Regel nicht gleichmäßig aus. Die Punkte können nur innere 80% des RGB-Cubes auffüllen, oder Sie können sich in einem niedrigeren dimensionalen vielfachen befinden. Wenn dies der Fall ist, können die zurück gestellten Polynomen einen schlechten Auftrag ausführen, um die Werte über die Datenpunkte hinaus zu extrapolieren. manchmal werden unrealistische Vorhersagen zurückgegeben. Sie möchten ein Modell, das immer relativ realistische Werte zurückgibt. Hierfür ist eine Methode erforderlich, mit der das Begrenzungs Verhalten von Regressions Polynomen effektiv gesteuert werden kann, indem den Polynomen, die sich in der Nähe der Grenze des RGB-Cubes befinden, zusätzliche Kosten entstehen. Ein weiteres Measure, mit dem sichergestellt wird, dass die Polynomen immer realistische Werte zurückgeben, wird durch Abschneiden der Ausgabe auf innerhalb des Cie-Spektral Lokus angewendet.

An diesem Punkt unterscheiden sich die scannermodellierung und die Kamera Modellierung voneinander. Es wird erwartet, dass das Kameramodell eine extrapolierte Region über die erfassten Punkte hinaus durchläuft, einschließlich der "Glanzlichter", die für das Scanner-Modell nicht erforderlich ist. Es wird erwartet, dass das scannerziel eine Ähnlichkeit abdeckt, die dem gedruckten Material ähnelt, das gescannt werden soll. Das Scanner-Modell muss in dem Sinne, dass es nicht unrealistische Werte zurückgeben sollte, immer noch robust sein, aber es ist nicht erforderlich, eine extra polierungs Version zu überschreiten. Um die Stabilität sicherzustellen, wird die oben genannte L-Polynoms um 100 abgeschnitten, d. h., das polynomal wird gezwungen, nicht über "DMin" des scannerziels hinaus zu extrapolieren.

Es wird erwartet, dass das Kameramodell zu Glanzlichtern extrapoliert, sodass Clipping bei 100 nicht erwünscht ist. Stattdessen wird der folgende Algorithmus verwendet.

Künstliche Steuerungs Punkte werden eingeführt, um das Verhalten der Polynomials in Regionen mit unzureichender Stichprobenentnahme zu steuern. Wenn Sie diese Steuerungs Punkte strategisch mit den entsprechenden Werten platzieren, können Sie die Polynomen in der gewünschten Richtung "abrufen". In der aktuellen Implementierung werden acht Steuerungs Punkte verwendet, die den Ecken des RGB-Cubes entsprechen. Wenn die Geräte Werte in Unity normalisiert werden, lauten die folgenden Punkte:

*R* = 0, *G* = 0, *B* = 0

*R* = 0, *G* = 0, *B* = 1

*R* = 0, *G* = 1, *B* = 0

*R* = 0. *G* = 1, *B* = 1

*R* = 1, *G* = 0, *B* = 0

*R* = 1, *G* = 0, *B* = 1

*R* = 1, *G* = 1, *B* = 0

*R* = 1, *G* = 1, *B* = 1

Mit Ausnahme von White *R*  = *G*  = *B* = 1, das einem CIELAB-Wert von *L* = 100, *u*  = *v* = 0 zugeordnet ist, wird der folgende Extraktions Algorithmus verwendet, um den entsprechenden CIELAB-Wert zu bestimmen, der zugeordnet werden soll. Im Allgemeinen wird für eine bestimmte (*r*,*g*,*b* ) eine Gewichtung mit jedem der (*r <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) im Stichproben DataSet verknüpft. Es gibt zwei Ziele, die Gewichtung zuzuweisen. Zuerst ist die Gewichtung umgekehrt proportional zu der Entfernung zwischen (*r*,*g*,*B* ) und (*r <sub>i</sub>*,*g <sub>i</sub>*,*b <sub>i</sub>* ). Zweitens: Sie möchten 0 (null) oder 0 (null) an Punkte verwerfen, die einen anderen Farbton als den angegebenen Punkt aufweisen (*R*,*G*,*B* ). Um den Farbton zu berücksichtigen, berücksichtigen Sie Punkte, die sich in einem Kegel befinden, dessen Scheitelpunkt bei (0,0) liegt, dessen Achse mit dem Zeilen Beitritt (0, 0, 0) zu (*R*,*G*,*B* ) und einem semivertikalen Winkel übereinstimmt. erfüllt COS? = 0,9. Eine Abbildung dieses Kegel finden Sie in Abbildung 3.

![Diagramm, das die Form der Umgebung anzeigt.](images/cdmp-lcd-dmp-figure3.png)

**Abbildung 3** : Filtern der Beispiel Punkte nach Winkel und Entfernung. Die Form der dargestellten Umgebung dient nur der Veranschaulichung. Die tatsächliche Form hängt von der verwendeten Entfernung ab. Wenn die 1-Norm verwendet wird, handelt es sich um eine rautenförmige Umgebung.

Innerhalb dieses Kegel wird eine zweite Filterung durchgeführt, die auf der RGB-Distanz basiert, die die durch

![Zeigt die Formel für das zweite Filtern im Kegel an.](images/cdmp-formula28.png)

Beim aktuellen Kegel ist die erste Suche nach Punkten, die innerhalb eines Entfernungs von 0,1 von (*R*,*G*,*B* ) liegen. Wenn in diesem RADIUS kein Punkt gefunden wird, wird der Radius um 0,1 erweitert, und die Suche wird neu gestartet. Wenn die nächsten Runden Netze keinen Punkt haben, wird der Radius um 0,1 erweitert. Dieser Prozess wird fortgesetzt, bis der RADIUS maxdist/5 überschreitet, wobei maxdist = 3 im Fall von 1-Norm liegt. Wenn kein Punkt gefunden wird, wird der Kegel durch Verringern der cos vergrößert? um 0,05, also das Erhöhen des Winkels? und den gesamten Prozess mit einem zunehmenden RADIUS neu starten. Dieser Prozess wird fortgesetzt, bis ein nicht leerer Satz von Punkten gefunden wird, oder COS? erreicht 0, d. h., der Kegel wurde als Ebene geöffnet. An diesem Punkt wird die Suche durch Erhöhen des RADIUS neu gestartet, mit der Ausnahme, dass die Suche so lange fortgesetzt wird, bis der RADIUS maxdist erreicht. Dadurch wird sichergestellt, dass im ungünstigsten Fall ein nicht leerer Satz von Punkten gefunden wird. Der Algorithmus wird im Flussdiagramm in Abbildung 4 zusammengefasst.

![Diagramm, das den Ablauf des Algorithmus anzeigt.](images/cdmp-lcd-dmp-figure4.png)

**Abbildung 4** : Flussdiagramm zum Bestimmen der in der extrapolierungs Gruppe verwendeten Beispiel Punkte für einen Eingabe-RGB-Wert

Angenommen, der vorherige Prozess ergibt eine nicht *leere Gruppe von* Punkten (*R <sub>i</sub>*,*G <sub>i</sub>*,*b <sub>i</sub>* ) und entsprechende (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), dann wird für jeden dieser Punkte eine Gewichtungs *w <sub>i</sub>* zugewiesen, angegeben durch

![Zeigt die Formel für eine Gewichtung für jeden Punkt an.](images/cdmp-formula29.png)

Schließlich wird der extrapolier definiert durch

![Zeigt die Definition für die extrapolier.](images/cdmp-formula30.png)

Die vorstehenden Gleichungen bilden eine Instanz der "mit umgekehrter Entfernung gewichteten Methoden", die in der Regel als Shepard-Methoden bezeichnet werden. Wenn Sie jeden der acht Punkte von EQ (6) über den Algorithmus ausführen, werden acht Steuerungs Punkte abgerufen, jeweils mit den Werten *R*,*G*,*b* und *L*,*a* und *B* , die mit den ursprünglichen Beispiel Daten in den Pool eingefügt werden.

Um sicherzustellen, dass das Modell immer gültige Farbwerte und die Systemintegrität und die Stabilität der gesamten farbverarbeitungs Pipeline generiert, müssen Sie ein endgültiges Abschneiden der Ausgabe des Polynoms-Modells durchführen. Der visuelle Bereich von Cie wird von der achrogmatischen Komponente (*Y* oder *L* ) und der chromatischen Komponente (*XY* oder *a' b '* beschrieben, die mit dem XYZ-Raum durch eine projektive Transformation verknüpft ist). In der aktuellen Implementierung wird die Chromatizität der *b ' b '* verwendet, da Sie direkt mit dem CIELUV-Raum verknüpft ist. Für jeden *CIELAB* -Wert wird " *L* " zuerst auf einen nicht negativen Wert zugeschnitten:

![Zeigt das Abschneiden von L auf einen nicht negativen Wert an.](images/cdmp-formula31.png)

Um das extrapolieren für Glanzlichter zu ermöglichen, wird *L* nicht um 100 abgeschnitten, d. h. die "konventionelle" Obergrenze für *L* im Lab-Bereich.

Wenn *L* = 0 ist, werden *a* und *b* abgeschnitten, sodass a *= b =* 0 ist. Wenn *L* ? 0, berechnen

![Zeigt die Formel an, wenn L = 0.](images/cdmp-formula32.png)

Dabei handelt es sich um die Komponenten eines Vektors im ' *b* '-Diagramm vom weißen Punkt (*u? '*,*v? '* ). ) auf die betreffende Farbe. Definieren Sie den Speicherort des Cie-Spektrums als die zusammen gezierte Hülle aller Punkte (*a '*,*b '* ), die durch die Wellenlinie parametrisiert werden?:

![Zeigt die Formel für die-Wellen Wellen an.](images/cdmp-formula33.png)

dabei ![ zeigt die Funktionen für den Cie-Farbabgleich an.](images/cdmp-formula34.png) die Funktionen der Cie-Farb Übereinstimmung für den 2-Grad-Beobachter. Wenn der Vektor außerhalb des Cie-Ursprung liegt, wird die Farbe auf den Punkt auf dem Cie-Lokus zugeschnitten, bei dem es sich um die Schnittmenge des Lokus und die durch den Vektor definierte Linie handelt. Weitere Informationen in Abbildung 5. Wenn Clipping aufgetreten ist, wird der *a* -Wert und der *b* -Wert durch erstes subtrahieren *eines?* -Werts rekonstruiert. und *b? "* aus dem abgeschnitten *a '* und *b '* und dann mit 13 *L* multipliziert.

![Diagramm, das das Diagramm für den clippingalgorithmus anzeigt.](images/cdmp-lcd-dmp-figure5.png)

**Abbildung 5** : Clipping-Algorithmus für Lab-Werte, die sich außerhalb des Sichtbarkeit von Cie befinden

In der aktuellen Implementierung wird der Cie-spektrallokus in der Ebene der *b ' b '* durch eine schrittweise lineare Kurve mit 35 Segmenten dargestellt (entsprechend einer Wellenlinie zwischen 360 nm und 700 nm). Wenn Sie die Liniensegmente so sortieren, dass ihre untergeordneten Winkel am weißen Punkt aufsteigend sind, was absteigender Wellenlinien entspricht, kann das Liniensegment, das sich mit dem durch den obigen Vektor geformten Strahl schneidet, durch eine einfache binäre Suche gefunden werden.

### <a name="rgb-printer-device-model-baseline"></a>Basislinie des RGB-Drucker Geräte Modells

Eine Geräte Charakterisierung eines RGB-Druckers besteht aus der Erstellung eines empirisch basierenden Modells des Geräts, das die geräteunabhängige CIELUV-Farbe für einen beliebigen RGB-Wert vorhersagt.

Es gibt zwei Möglichkeiten, das empirische Modell zu erstellen. Eine Möglichkeit besteht darin, die Gerätedaten für einen RGB-Drucker zu verwenden, und das andere die Verwendung analytischer Parameterdaten. Im ersten wird die von einem Benutzer für ein RGB-Druckergerät bereitgestellte Messungs Daten verwendet, um eine 3D-Nachschlage Tabelle (Data-D Suche Table, LUT) zu erstellen. Die Mess Daten bestehen aus XYZ-Werten für bei gleichmäßigen Stichproben von RGB-Patches. Typische Stichprobengrößen sind für jede Komponente 9 oder 17. Jeder Patch wird mit einem Farbwert oder einem Spektrophotometer im CIEXYZ-Raum gemessen. Der XYZ-Wert für einen Patch wird dann in einen CIELUV-Wert konvertiert, der einen 3D-LUT bildet. Im Gerätemodell wird die Methode "tetrahedral Interpolationsmethode" von Sakamoto auf den 3D-Kanal angewendet, um die CIELUV-Daten für eine bestimmte RGB-Daten vorherzusagen. (Erteilen Sie die US-Patent 4275413 (Sakamoto et al.), US-Patent 4511989 (Sakamoto), Kang \[ 1 \] . Die zwei erwähnten Patente sind abgelaufen.) Bei den in der zweiten Methode übergebenen analytischen Parameterdaten handelt es sich einfach um einen zuvor erstellten LUT. In der Regel wurde dieser LUT mithilfe der ersten Methode erstellt, obwohl er möglicherweise Hand erstellt wurde.

In der aktuellen Farbverwaltung wird die Quell Zuordnung als die Zuordnung definiert, die von RGB-Leerraum zu einem geräteunabhängigen CIEXYZ-Farbraum übergeht. Die Ziel Zuordnung wird als die Zuordnung definiert, die vom geräteunabhängigen CIEXYZ-Farbraum zu RGB-Speicherplatz reicht. Dies ist die Umkehrung der Quell Zuordnung.

Das empirische Modell wird direkt in der Quell Zuordnung verwendet. Zuerst werden die angegebenen RGB-Daten einer CIELUV-Daten zugeordnet, die in XYZ-Daten konvertiert werden. In der Ziel Zuordnung werden geräteunabhängige CIEXYZ-Daten zuerst in CIELUV-Daten konvertiert. Anschließend werden das empirische Modell und die klassische Newton-Raphson-Methode verwendet, um die besten RGB-Daten für die CIELUV-Daten vorherzusagen. Die Details zur Konvertierung von CIELUV in RGB-Daten lauten wie folgt:

Nachdem Sie einen 3D-Kanal von RGB zu CIELUV erstellt haben, wird die Zuordnung zwischen RGB und Luv mithilfe der tetrahedral-interpolung auf RGB erstellt. Diese Zuordnung wird durch die folgenden Gleichungen bezeichnet:

![Zeigt die Gleichungen für die Karte von R G B bis L U V an.](images/cdmp-image125.png)

Die Inversion der Zuordnung besteht aus der Lösung für beliebige Farben. ![Zeigt L U V an.](images/cdmp-image127.png) , das folgende System nichtlinearer Gleichungen:

![Zeigt die nichtlinearen Gleichungen für das lolving beliebiger Farbe L U V an.](images/cdmp-image129.png)

Eine nichtlineare Gleichung, die auf der klassischen Newton-Raphson-Methode basiert, wird im neuen allgemeinen Tabellen Ausdruck (CTE) verwendet. Ein ursprünglicher Schätzwert bzw. *a* -Wert, der <sub>vor</sub> (R 0, G 0, B 0) liegt, wird durch Durchsuchen einer "Seed Matrix" abgerufen, die aus einem einheitlichen 8x8x8-Raster mit vorab berechneten (RGB-, Luv-) Paaren besteht. Die entsprechende RGB-Luv, die der L u v am nächsten ist, \* \* \* wird ausgewählt. Jeder Punkt in der Seed-Matrix entspricht dem Mittelpunkt einer Zelle, sodass die Iterationen nicht mit einem Punkt an der Begrenzungs Seite des RGB-Cubes beginnen. Mit anderen Worten: der RGB der Kerne wird durch Folgendes definiert: Schritt = 1/8 s <sub>IJK</sub> = (Schritt/2 + (i-1) Schritt, Schritt/2 + (j-1) Schritt, Schritt/2 + (k-1) Schritt) mit i, j, k = 1... 8 im *i* . Schritt von Newton-Raphson zeigt die nächste Schätzung ![ die Variablen für die nächste Schätzung an.](images/cdmp-image133.png) wird von der Formel abgerufen:

![Zeigt die Formel für die Schätzung an.](images/cdmp-image135.png)

Die Iteration wird beendet, wenn der Fehler (Entfernung im CIELUV-Bereich) kleiner ist als eine voreingebene Toleranzstufe (0,1 im CTE) oder wenn die Anzahl der Iterationen die maximal zulässige Anzahl von Iterationen überschreitet (10 in der CTE). Die Werte für die Toleranz und die Anzahl der Iterationen wurden empirisch als wirksam festgelegt. In zukünftigen Versionen kann der Toleranzwert geändert werden.

Die Jacobian-Matrix wird mithilfe der Forward-Differenz berechnet, außer an einem Begrenzungs Punkt (mindestens eine R, G, B ist 1), wobei der abwärts Unterschied stattdessen verwendet wird. Anstatt die Umkehrung der Jacobian-Matrix zu berechnen, wird das lineare System mithilfe der Gauss-Jordan Beseitigung mit vollständigem pivotieren direkt gelöst.

Am Ende der Iterationen wird die Konvergenz möglicherweise noch nicht erreicht, da Newton-Raphson ein "lokaler" Algorithmus ist, das heißt, dass Sie nur dann gut funktioniert, wenn Sie mit einer anfänglichen Schätzung beginnen, die in der Nähe der echten Lösung liegt. Wenn am Ende der Newton-Raphson Iterationen die Konvergenz innerhalb der vordefinierten Fehlertoleranz nicht erreicht wurde, werden die Iterationen mit einem neuen Satz von Kernen neu gestartet, die wie folgt definiert werden.

Die bisher beste Lösung ist beispielsweise (r, g, b). Aus dieser Lösung werden n a-posteriori-Kerne abgeleitet, wobei n = 4 ist. Die Projekt Mappe wird intuitiv in eine Schrittgröße verschoben, die von N abhängig ist. Siehe Abbildung 6.

![Diagramm, das die Richtung der Projekt Mappe enthält.](images/cdmp-image136.png)

**Abbildung 6** : die Zuordnungs Richtung der Lösung hängt davon ab, in welchem Octant Sie sich befindet.

Anders ausgedrückt: wenn r &gt; 0,5, wird der Wert im r-Kanal verringert; andernfalls wird der Wert angehoben. Es gibt eine ähnliche Logik für die Kanäle "G" und "B". Die genauen Definitionen lauten:

Perturbation = 0.5/(N + 1)

Dir (r) =-1, wenn r &gt; 0,5; + 1 andernfalls. Gleiches gilt für dir (g) und dir (b).

Der Jth a posteriori Seed, s????, ist (r + dir (r) \* j \* Perturbation, g + dir (g) \* j \* Perturbation, b + dir (b) \* j \* Perturbation)

Testen Sie die ersten s???? Wenn eine neue Projekt Mappe in der Fehlertoleranz angezeigt wird, können Sie den Vorgang abbrechen. Andernfalls können Sie die zweiten s???? usw., bis die n-ten????.

Die schematiken des gesamten Algorithmus sind in Abbildung 7 dargestellt.

![Diagramm, das den Ablauf für das Umkehren des Geräte Modells anzeigt.](images/cdmp-image138.png)

**Abbildung 7** : schematiken zum Umkehren des Geräte Modells

### <a name="rgb-virtual-device-model-baseline"></a>Grundlegende Konfiguration des virtuellen Geräte Modells

Bei diesem Gerätemodell (DM) handelt es sich um einen einfachen Matrix-/Ton-Reproduktions Algorithmus. Die Matrix wird aus dem weißen Punkt und den primären Replikaten mithilfe von standardmäßigen Color Science-Algorithmen abgeleitet. Die audioreproduktions Kurve wird von den Messparametern gemäß den ICC-Beschreibungen von Cursor Type und ParameterType abgeleitet (oder bei Bedarf umgekehrt). Details zu den internen Algorithmen werden nach der zusätzlichen Validierung von Problemen mit hohem dynamischen Bereich bereitgestellt.

Das virtuelle RGB-Gerätemodell ist eine idealisierte Matrix-/Ton-Reproduktions Kurve (RGB), ähnlich wie bei einem Matrix basierten Entwurf mit drei Komponenten. Die "Virtual Measurement"-Parameter der DM enthalten einen weißen Punkt Wert (absolute CIEXYZ), RGB-Primärwerte (absolute CIEXYZ) und eine Ton-Reproduktions Kurve, die auf dem hashparameterype und dem Cursor Type in der XML-Formatierung basiert, die mit den DMP-Schemas konsistent ist.

In der folgenden Tabelle sind die-Funktionstyp Codierung für den Parameter "-Parametertyp" und die entsprechende Unterstützung in "irigbvirtualdevicemodelbase" aufgeführt.



| Funktionstyp                                         | Parameter                          | type                                     | Hinweis                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Zeigt die Funktion "gammatype" an.](images/cdmp-image154.png)<br/> | g<br/>              | Gammatype<br/>                 | Allgemeine Implementierung<br/>           |
| ![Zeigt die Funktion "gammaoffsetgaintype" an.](images/cdmp-image156.png)<br/> | GA b<br/>           | Gammaoffsetgaintype<br/>       | Cie 122-1966<br/>                    |
| ![Zeigt die Funktion ' gammaoffsetgainoffsettype ' an.](images/cdmp-image158.png)<br/> | GA b c<br/>         | Gammaoffsetgainoffsettype<br/> | IEC 61966-3<br/>                     |
| ![Zeigt die Funktion "gammaoffsetgaingaintype" an.](images/cdmp-image160.png)<br/> | GA b c d<br/>       | Gammaoffsetgaingaintype<br/>   | IEC 61966-2.1<br/> sRGB<br/> |
| ![Zeigt eine Funktion für die Parameter "g a b c d e f" an.](images/cdmp-image162.png)<br/> | GA b c d e f<br/>   | –<br/>                       | In WCS nicht unterstützt<br/>            |



 

Die audiokurve für virtuelle RGB-Geräte wird in deviceumcolormetric zwischen den Eingabedaten, pdebug-Elementen und der Matrix Multiplikation angewendet. Für "colormetricydevice" muss eine Methode zum Umkehren der Tonkurve verwendet werden. In der baselineimplementierung erfolgt dies durch direkte Interpolationen in derselben für deviceumcolormetric verwendeten Tonkurve.

Die Kurven sollten in den Profilen als Paare von Zahlen in float-Raum angegeben werden. Die erste Zahl stellt Werte in PDE vicecolors dar. Die zweite Zahl stellt die Ausgabe der Tonkurve dar. Alle Werte in der Tonkurve müssen zwischen mincolorantused und maxcolorantused liegen. Die Tone-Kurven müssen mindestens zwei Einträge enthalten: eine für mincolorantused und eine für maxcolorantused. Die maximale Anzahl von Einträgen in der tonecurve beträgt 2048. Im Allgemeinen können Sie mit der größeren Anzahl von Einträgen in der Tabelle die Krümmung genauer modellieren. Zwischen den Einträgen wird eine schrittweise lineare Interpolationen ausgeführt.

Sie können alternative Interpolations Methoden in Erwägung gezogen. Wenn Sie etwas über das zugrunde liegende Verhalten des Geräts wissen, können Sie mit einer höheren Bestell Kurve weniger Stichproben und ein genaueres Modell verwenden. Wenn Sie jedoch den falschen Kurstyp verwenden, sind Sie sehr ungenau. Ohne weitere Informationen können Sie den Kurven Typ nicht erraten. Verwenden Sie daher lineare Interpolationen, und stellen Sie viele Datenpunkte bereit.

### <a name="cmyk-printer-device-model-baseline"></a>Baseline des CMYK-Drucker Geräte Modells

Eine Geräte Charakterisierung eines CMYK-Druckers besteht aus der Konstruktion eines empirisch verwendeten Modells des Geräts, das die gedruckte Farbe für einen beliebigen CMYK-Wert vorhersagt. Die-Charakterisierung umfasst auch die Inversion dieses Modells, sodass ein Rezept des CMYK-Werts für eine angegebene zu druckende Farbe angegeben werden kann. Dies wird in der Regel in Bezug auf CIEXYZ oder CIELAB-Wert definiert.

In der Regel wird ein IT-8,7/3-Ziel mit CMYK-Patches verwendet. Die Patches bestehen aus der Stichprobenentnahme des CMYK-Speicherplatzes in einer klar definierten Weise, sodass ein rechteckiges Raster (mit nicht einheitlichem Abstand in C, M, Y und K) gebildet wird. Jeder Patch wird dann mit einem farbigen oder einem spektrophoto Meter gemessen. Die Messungen in CIEXYZ-Werten bilden dann eine Suche Table (LUT), aus der ein empirisches Modell des Druckers mit der Interpolationsmethode von Sakamoto erstellt wird. US-Patent 4275413 (Sakamoto et al.), US-Patent 4511989 (Sakamoto), Kang \[ 1 \] . Die zwei erwähnten Patente sind abgelaufen.

Bestimmte Anforderungen an die CMYK-maßproben, die erforderlich sind, damit ein Gerätemodell Profil vom CMYK-druckerbaseline-Gerätemodell als gültig akzeptiert wird, lauten wie folgt. (Die Stichproben Menge wird in den meisten Fällen als Satz von CMY-Beispielcubes beschrieben, die jeweils mit einer bestimmten K-Ebene verknüpft sind.)

-   Es müssen mindestens gültige CMY-Cubes für die Ebenen K = 0 und k = 100 bereitgestellt werden.
-   Zwischen K-Ebenen dürfen nicht gleichmäßig verteilt werden.
-   Alle zwischen-K-Ebenen ohne gültigen CMY-Cube werden ignoriert.
-   Die CMY-Cubes verwenden möglicherweise nicht einheitliche Stichproben Intervalle (Raster Abstände), aber der gleiche Satz von Stichproben Intervallen muss in allen C-, M-und Y-Dimensionen des CMY-Cubes für eine bestimmte K-Ebene verwendet werden.
-   Jeder K-Level-CMY-Cube kann eine andere Anzahl und einen anderen Abstand von Beispiel Intervallen verwenden.
-   Alle CMY-Cubes müssen die "Ecken" des CMY-Cubes enthalten, d. h. CMY Samples bei \[ 0, 0, 0 \] , \[ 0, 0100 \] , \[ 0100, 0 \] , \[ 100, 0, 0 \] , \[ 0100.100 \] , \[ 100, 0100 \] , \[ 100.100, 0 \] , \[ 100.100.100 \] .
-   Alle mittleren CMY-Raster Ebenen müssen in jedem Kanal vollständig abgetastet werden. Anders ausgedrückt: ein Beispiel muss bei jeder 3D-Raster Überschneidung innerhalb des CMY-Cubes vorhanden sein.
-   Für k = 0 und k = 100 CMY-Cubes sind 2 x 2x2-Cubes, die nur Ecken sind, als gültig akzeptiert.

    \[Hinweis: für k = 0 und k = 100 Ebenen wird ein 3x3x3-Cube als 2x2x2-Cube verarbeitet. die zwischen Abtast Ebene wird ignoriert. für 4 x 4X4 und größere Cubes werden alle on-Grid-Beispiele verwendet.\]

-   Für zwischen-K-Ebenen sind 4x4x4-CMY-Cubes die Mindestanzahl, die als gültig akzeptiert wird.

Ein qualitativ hochwertiges Profil verwendet präzisere Stichproben Raster als das minimal erforderliche, das in der Regel 9x9x9x9 oder höher ist. Die Beispiele der Ziele IT 8.7/3, IT 8.7/4 und ECI erstellen gültige Gerätemodell profile (DMPs) für das Gerätemodell des CMYK-druckerbaseline. Obwohl dieses Gerätemodell in der Lage ist, die überflüssigen (Off-Grid)-Beispiele in diesen Zielen zu ignorieren, ist es nicht garantiert, dass dies für andere Ziele möglich ist, und daher wird empfohlen, dass Sie aus maßsätzen entfernt werden, die in Profile für dieses Gerätemodell übernommen werden.

Die Inversion des Drucker Modells stellt weitere Schwierigkeiten dar. Wenn eine Eingabe Farbe in ciecam vorliegt, gibt es eine Frage, ob sich diese Farbe im Drucker Spiel befindet. Außerdem gibt es das Problem bezüglich der Anordnung von Punkten im Farb Darstellungs Bereich. Die CMYK-Werte können zwar so angeordnet werden, dass Sie auf ein rechteckiges Raster fallen, wie dies im Ziel der IT-Version 8.7/3 der Fall ist. das gleiche gilt jedoch nicht für die sich ergebenden gedruckten Farben, da Sie sich im Raum der Farbdarstellung befinden. Im Allgemeinen sind Sie im Farb Darstellungs Raum ohne bestimmtes Muster verstreut.

Im Allgemeinen gibt es zwei Ansätze für das Inversion-Problem von verstreuten Punkten. Ein Ansatz besteht in der Verwendung einer geometrischen Unterteilung des Drucker Farbskala mithilfe von elementaren dreidimensionalen Festkörpern, wie z. b. "tetrahedra". Eine Unterteilung des Drucker Bereichs im Farb Darstellungs Bereich kann aus der entsprechenden unter Division des CMY-Speicherplatzes (K) abgeleitet werden. Weitere Informationen finden Sie unter nicht reagiert \[ 93 \] , Kang \[ 97 \] . Diese Vorgehensweise hat den Vorteil, dass die Einfachheit der Komplexität liegt. Im Fall eines Tetrahedron werden in einer Interpolations Weise nur vier Punkte verwendet. Andererseits hängt das Ergebnis stark von einigen Punkten ab, was bedeutet, dass ein Messfehler eine bedeutende Auswirkung auf das Ergebnis hat. Der interpolant ist auch tendenziell nicht so reibungslos. Der zweite Ansatz nimmt keine Unterteilung an und basiert auf der Technik der verstreuten Daten interpolung. Ein klassisches Beispiel ist die Technik der Shepard-Interpolationsmethode oder eine umgekehrte gewichtete Methode (siehe Shepard \[ 68 \] ). Hier werden einige Punkte, die den Eingabe Punkt betreffen, auf irgendeine Weise ausgewählt, wobei jeder eine Gewichtung zugewiesen wird, in der Regel umgekehrt proportional zur Entfernung, und der interpolant als gewichteter Durchschnitt der benachbarten Punkte genommen wird. Bei dieser Vorgehensweise ist die Wahl der benachbarten Punkte von entscheidender Bedeutung für die Leistung. Obwohl zu wenige Punkte den interpolanten ungenau und nicht glatt darstellen können, erzwingen zu viele Punkte eine hohe Rechenleistung, da die Gewichtungen in der Regel nichtlineare Funktionen sind und aufwändig berechnet werden.

Bei den beiden oben beschriebenen Ansätzen treten Probleme auf. Der Ansatz der Unterteilung hängt in der Regel von den Daten ab, die relativ reibungslos sind, und in der Regel ist der interpolant nicht sehr reibungslos. Die verstreute Daten interpolung ist eher toleranter als das Daten Rauschen und sorgt im Allgemeinen für eine reibungslosere interpolante, aber Sie ist rechnerisch kostengünstiger.

Der neue CTE hat einen alternativen Ansatz. Das CMYK-Gerät wird als Sammlung von mehreren CMY-Geräten behandelt, von denen jeder einen bestimmten Wert Black (K) hat. Bei Verwendung eines Auswahl Algorithmus, der als Parameter Helligkeit und Chroma verwendet wird, wird eine schwarze Ebene ausgewählt. Die CMY-Werte werden von der Inversion der entsprechenden CMY-zu Luv-Tabelle mithilfe der Newton-Methoden abgerufen, die an anderer Stelle vom RGB-Drucker Algorithmus verwendet werden.

Führen Sie die folgenden Schritte aus.

1.  Drucken Sie das Ziel für die Charakterisierung, d. h. das Ziel "IT 8.7/3", oder ein Ziel, das eine Stichprobe des CMYK-Raums in regelmäßigen oder nicht regelmäßigen Abständen enthält.
2.  Messen Sie das Ziel mithilfe eines spektrophoto meters, und konvertieren Sie die Messungen in CIELUV-Raum.
3.  Erstellen Sie die vorwärts Zuordnung von CMYK zu Luv.
4.  Verwenden Sie die vorwärts Zuordnung, um einen Satz von CMY für Luv-Zuordnungen für einen Bereich von K-Werten zu erstellen.
5.  Für jeden Eingabe-Luv-Wert wird der entsprechende CMYK-Wert abgerufen, indem eine der in Schritt 4 oben erstellten Zuordnungen ausgewählt und mit der-Methode von Newton zum Abrufen eines CMY Colorant-Satzes verwendet wird, der den ausgewählten K-Wert begleitet.

Die Schritte 1 und 2, bei denen es sich um Standardverfahren handelt, werden von einem Profil Erstellungs Programm ausgeführt, das nicht Teil des neuen CTE ist. Das Ziel "IT 8.7/3" enthält eine relativ detaillierte Stichprobe aller CMYK-Werte auf verschiedenen Ebenen von C, M, Y und k. Alternativ kann ein benutzerdefiniertes Ziel mit einheitlicher Stichprobenentnahme der C-, m-, y-und k-Kanäle verwendet werden. Nachdem das Ziel gedruckt wurde, kann ein "spektrophoto eter" oder ein "colormeter" verwendet werden, um den XYZ-Wert jedes Patches zu messen, und der XYZ-Wert kann mithilfe des CIELUV-Modells in den Luv-Wert konvertiert werden.

Schritt 3: die Konstruktion des vorwärts Bilds von CMYK zu Luv kann erreicht werden, indem alle bekannten Interpolations Techniken, wie z. b. "tetrahedral" oder "Multilinear", auf dem rechteckigen Raster im CMYK-Raum angewendet werden. Im neuen allgemeinen Tabellen Ausdruck wird eine 4-dimensionale tetrahedral-Interpolations Datei verwendet. Da sich die CMY-Samplings in der Regel auf jeder Ebene von K unterscheiden, verwenden wir eine Technik der Super-Stichprobenentnahme, wie unten beschrieben. Bei einem bestimmten CMYK-Punkt werden die k-Ebenen auf der Ebene zuerst basierend auf dem k-Wert bestimmt. Führen Sie dann ein "Super Grid" auf jeder k-Ebene aus, bei der es sich um eine Kombination der CMY-Raster auf den beiden Ebenen handelt. Auf jeder k-Ebene wird der Luv-Wert jedes neu eingeführten Raster Punkts durch eine dreidimensionale, in dieser k-Ebene erstellbare multiinterpolations-Interpolations Stufe abgerufen. Zum Schluss wird eine 4-dimensionale tetrahedral-interpolung für den jeweiligen CMYK-Punkt in diesem neuen Raster ausgeführt.

![Diagramm, das Supersampling anzeigt.](images/cdmp-image163.png)

**Abbildung 8** : Supersampling

In Schritt 4 wird eine Reihe von CMY-zu-Luv-Nachschlage Tabellen (LUTs) erstellt. Die in Schritt 3 erstellte vorwärts Zuordnung wird wiederholt aufgerufen, um den CMYK-Speicher neu zu testen. Der CMYK-Farbraum wird mit einem geraden Abstand von K und einem anderen, aber immer noch gleichmäßig belegten Sampling von CMY entnommen.

Schritt 5 ist ein Verfahren zum Abrufen des CMYK-Werts mithilfe der in Schritt 4 erstellten LUTs für jeden Eingabe-Luv-Punkt. Der geeignete Wert von K wird ausgewählt, indem die Helligkeit und der Grad der Farbe in der angeforderten Luv analysiert werden. Nachdem die Tabelle ausgewählt wurde, werden die CMY-Werte mithilfe der Newton-Methode aus der Tabelle abgerufen (wie zuvor unter dem RGB-Drucker Gerätemodell dokumentiert).

Der CIELUV-Speicherplatz wird im Drucker Modell anstelle von ciejab verwendet, da das Gerätemodell ausschließlich auf den im DMP verfügbaren farbmetrikdaten basieren soll. Das DMP enthält farbige Metrikdaten für jeden gemessenen Patch, einschließlich des Medien weißen Punkts. Daher ist es möglich, CIEXYZ-Daten in CIELUV-Daten zu konvertieren. Es ist jedoch nicht möglich, in CIECAM02 Jch oder Jab zu konvertieren, da es keinen Zugriff auf die Informationen in der Anzeige Bedingung in der DMP gibt.

### <a name="rgb-projector-device-model-baseline"></a>Basislinie des RGB-projektorgeräts

Hinweis: viele RGB-Projektoren haben mehr als einen Betriebsmodus. In einem Modus, bei dem es sich oft um die Standardeinstellung handelt, die beispielsweise als "Präsentation" bezeichnet werden kann, wird die Farb Antwort des Projektor für maximale Helligkeit optimiert. In diesem Modus verliert der Projektor jedoch die Möglichkeit, helle und leicht zu verächende Farben (z. b. blendtöne und einige fleischfarben) zu reproduzieren. Der Projektor ist in einem anderen Modus, der häufig als "Film", "Video" oder "sRGB" bezeichnet wird, für die Reproduktion realistischer Bilder und natürlicher Szenen optimiert. In diesem Modus wird die maximale Helligkeit abgehandelt, um die Gesamtqualität der Farb Reproduktion zu verbessern. Um eine zufriedenstellende Farb Reproduktion mit RGB-Projektoren zu erhalten, ist es erforderlich, den Projektor in einem Modus zu platzieren, in dem eine Glättung von Farben wiedergegeben werden kann.

![Diagramm mit einem D L P-Gerätemodell.](images/cdmp-image167.png)

**Abbildung 9** : DLP-Gerätemodell

Ein eingehender RGB-Wert übergibt zwei Berechnungs Pfade. Der erste ist das Matrix Modell, das zu einem XYZ-Wert führt. Danach folgt die Konvertierung von XYZ in Luv. Die zweite ist die nicht einheitliche LUT-interpolung mit der tetrahedral-interpolung. Die Ausgabe der Interpolation befindet sich bereits im Luv-Raum durch Konstruktion. Die beiden Ausgaben werden hinzugefügt, um den vorhergesagten Luv-Wert zu erhalten. Diese wird schließlich in XYZ konvertiert. Dies ist die erwartete Ausgabe des Farb Metrik Modells für das DLP-Gerät.

Da Projektoren Geräte anzeigen, unterstützen Sie auch die Inversion des Modells, d. h. die Transformation von XYZ zu RGB. Da das Gerätemodell RGB-Speicherplatz in XYZ-Leerraum umwandelt, bei dem es sich um dreidimensionale handelt, entspricht Inversion der Behebung von drei nichtlinearen Gleichungen in drei unbekannten Zeichen. Dies kann durch standardmäßige Formel-und Lösungsverfahren wie Newton-Raphson erreicht werden. Es ist jedoch vorzuziehen, zuerst XYZ in Luv zu konvertieren und dann die Luv in RGB-Transformation umzukehren, da der Luv-Speicher eher perperer linear ist als XYZ-Leerraum.

### <a name="icc-device-model-baseline"></a>Basislinie des Modells für das Modell

Die Initialisierungsfunktion für den Workflow des Workflows wird durch Erstellen eines speziellen Gerätemodell Profils für das ICC-Gerät aktiviert, das das Profil Objekt speichert und eine ICC-Transformation mit einem No-op XYZ-Profil erstellt. Diese Transformation wird dann verwendet, um zwischen Geräte-und CIEXYZ-Farben zu übersetzen.

![Das Diagramm zeigt die Interoperabilität zwischen c i T E i c c-Workflow.](images/cdmp-image168.png)

**Abbildung 10** : zitieren der Interoperabilität von Workflow Workflows

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der grundlegenden Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[Windows Color System: Schemas und Algorithmen](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





