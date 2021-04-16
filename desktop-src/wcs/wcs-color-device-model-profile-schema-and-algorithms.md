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
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a><span data-ttu-id="d252a-118">WCS-Farbgerätemodell: Profilschema und Algorithmen</span><span class="sxs-lookup"><span data-stu-id="d252a-118">WCS Color Device Model Profile Schema and Algorithms</span></span>

<span data-ttu-id="d252a-119">Dieses Thema enthält Informationen zum WCS-Farb Gerätemodell-Profil Schema und den zugehörigen Algorithmen.</span><span class="sxs-lookup"><span data-stu-id="d252a-119">This topic provides information about the WCS Color Device Model Profile Schema and its associated algorithms.</span></span>

<span data-ttu-id="d252a-120">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="d252a-120">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d252a-121">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d252a-121">Overview</span></span>](#overview)
-   [<span data-ttu-id="d252a-122">Architektur des Farb Gerätemodell Profils</span><span class="sxs-lookup"><span data-stu-id="d252a-122">Color Device Model Profile Architecture</span></span>](#color-device-model-profile-architecture)
-   [<span data-ttu-id="d252a-123">Das CDMP-Schema</span><span class="sxs-lookup"><span data-stu-id="d252a-123">The CDMP Schema</span></span>](#the-cdmp-schema)
-   [<span data-ttu-id="d252a-124">WCS CDMP v 2.0-Kalibrierungs Addition</span><span class="sxs-lookup"><span data-stu-id="d252a-124">WCS CDMP v2.0 Calibration Addition</span></span>](#wcs-cdmp-v20-calibration-addition)
-   [<span data-ttu-id="d252a-125">Die CDMP-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="d252a-125">The CDMP Schema Elements</span></span>](#the-cdmp-schema-elements)
    -   [<span data-ttu-id="d252a-126">Colordevicemodelprofile</span><span class="sxs-lookup"><span data-stu-id="d252a-126">ColorDeviceModelProfile</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="d252a-127">Colordevicemodel</span><span class="sxs-lookup"><span data-stu-id="d252a-127">ColorDeviceModel</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="d252a-128">Namespaceversion</span><span class="sxs-lookup"><span data-stu-id="d252a-128">NamespaceVersion</span></span>](#namespaceversion)
    -   [<span data-ttu-id="d252a-129">Version</span><span class="sxs-lookup"><span data-stu-id="d252a-129">Version</span></span>](#namespaceversion)
    -   [<span data-ttu-id="d252a-130">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d252a-130">Documentation</span></span>](#documentation)
    -   [<span data-ttu-id="d252a-131">Crtdevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-131">CRTDevice element</span></span>](#crtdevice-element)
    -   [<span data-ttu-id="d252a-132">Lcddevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-132">LCDDevice element</span></span>](#lcddevice-element)
    -   [<span data-ttu-id="d252a-133">Projector Device-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-133">ProjectorDevice element</span></span>](#projectordevice-element)
    -   [<span data-ttu-id="d252a-134">Scannerdevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-134">ScannerDevice element</span></span>](#scannerdevice-element)
    -   [<span data-ttu-id="d252a-135">Cameradevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-135">CameraDevice element</span></span>](#cameradevice-element)
    -   [<span data-ttu-id="d252a-136">Rgbprinterdevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-136">RGBPrinterDevice element</span></span>](#rgbprinterdevice-element)
    -   [<span data-ttu-id="d252a-137">Cmykprinterdevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-137">CMYKPrinterDevice element</span></span>](#cmykprinterdevice-element)
    -   [<span data-ttu-id="d252a-138">Rgbvirtualdevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-138">RGBVirtualDevice element</span></span>](#rgbvirtualdevice-element)
    -   [<span data-ttu-id="d252a-139">Pluginde vicetype</span><span class="sxs-lookup"><span data-stu-id="d252a-139">PlugInDeviceType</span></span>](#plugindevicetype)
    -   [<span data-ttu-id="d252a-140">Rgbvirtualmessrementtype</span><span class="sxs-lookup"><span data-stu-id="d252a-140">RGBVirtualMeasurementType</span></span>](#rgbvirtualmeasurementtype)
    -   [<span data-ttu-id="d252a-141">Gammatype</span><span class="sxs-lookup"><span data-stu-id="d252a-141">GammaType</span></span>](#gammatype)
    -   [<span data-ttu-id="d252a-142">Gammaoffsetgaintype</span><span class="sxs-lookup"><span data-stu-id="d252a-142">GammaOffsetGainType</span></span>](#gammaoffsetgaintype)
    -   [<span data-ttu-id="d252a-143">Gammaoffsetgainlineargaintype</span><span class="sxs-lookup"><span data-stu-id="d252a-143">GammaOffsetGainLinearGainType</span></span>](#gammaoffsetgainlineargaintype)
    -   [<span data-ttu-id="d252a-144">Toneresponsecurvestype</span><span class="sxs-lookup"><span data-stu-id="d252a-144">ToneResponseCurvesType</span></span>](#toneresponsecurvestype)
    -   [<span data-ttu-id="d252a-145">Gamutboundarysamplestype</span><span class="sxs-lookup"><span data-stu-id="d252a-145">GamutBoundarySamplesType</span></span>](#gamutboundarysamplestype)
    -   [<span data-ttu-id="d252a-146">Floatpaarlist</span><span class="sxs-lookup"><span data-stu-id="d252a-146">FloatPairList</span></span>](#floatpairlist)
    -   [<span data-ttu-id="d252a-147">Cmykprintermessbare rementtype</span><span class="sxs-lookup"><span data-stu-id="d252a-147">CMYKPrinterMeasurementType</span></span>](#cmykprintermeasurementtype)
    -   [<span data-ttu-id="d252a-148">Rgbprintermessbare rementtype</span><span class="sxs-lookup"><span data-stu-id="d252a-148">RGBPrinterMeasurementType</span></span>](#rgbprintermeasurementtype)
    -   [<span data-ttu-id="d252a-149">Rgbcapturemessrementtype</span><span class="sxs-lookup"><span data-stu-id="d252a-149">RGBCaptureMeasurementType</span></span>](#rgbcapturemeasurementtype)
    -   [<span data-ttu-id="d252a-150">Onebasedindex</span><span class="sxs-lookup"><span data-stu-id="d252a-150">OneBasedIndex</span></span>](#onebasedindex)
    -   [<span data-ttu-id="d252a-151">Rgbprojector messrementtype</span><span class="sxs-lookup"><span data-stu-id="d252a-151">RGBProjectorMeasurementType</span></span>](#rgbprojectormeasurementtype)
    -   [<span data-ttu-id="d252a-152">Displaymessrementtype</span><span class="sxs-lookup"><span data-stu-id="d252a-152">DisplayMeasurementType</span></span>](#displaymeasurementtype)
    -   [<span data-ttu-id="d252a-153">Messrementconditionstype</span><span class="sxs-lookup"><span data-stu-id="d252a-153">MeasurementConditionsType</span></span>](#measurementconditionstype)
    -   [<span data-ttu-id="d252a-154">Geometrytype</span><span class="sxs-lookup"><span data-stu-id="d252a-154">GeometryType</span></span>](#geometrytype)
    -   [<span data-ttu-id="d252a-155">Rgbprimariesgroup</span><span class="sxs-lookup"><span data-stu-id="d252a-155">RGBPrimariesGroup</span></span>](#rgbprimariesgroup)
    -   [<span data-ttu-id="d252a-156">Nonnegativecmyksampletype</span><span class="sxs-lookup"><span data-stu-id="d252a-156">NonNegativeCMYKSampleType</span></span>](#nonnegativecmyksampletype)
    -   [<span data-ttu-id="d252a-157">Nonnegativergbsampletype</span><span class="sxs-lookup"><span data-stu-id="d252a-157">NonNegativeRGBSampleType</span></span>](#nonnegativergbsampletype)
    -   [<span data-ttu-id="d252a-158">Nonnegativecmyktype</span><span class="sxs-lookup"><span data-stu-id="d252a-158">NonNegativeCMYKType</span></span>](#nonnegativecmyktype)
    -   [<span data-ttu-id="d252a-159">Nonnegativergbtype</span><span class="sxs-lookup"><span data-stu-id="d252a-159">NonNegativeRGBType</span></span>](#nonnegativergbtype)
    -   [<span data-ttu-id="d252a-160">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d252a-160">ExtensionType</span></span>](#extensiontype)
    -   [<span data-ttu-id="d252a-161">Nonnegativexyztype</span><span class="sxs-lookup"><span data-stu-id="d252a-161">NonNegativeXYZType</span></span>](#nonnegativexyztype)
    -   [<span data-ttu-id="d252a-162">Xyztype</span><span class="sxs-lookup"><span data-stu-id="d252a-162">XYZType</span></span>](#nonnegativexyztype)
-   [<span data-ttu-id="d252a-163">Die CDMP-baselinealgorithmen</span><span class="sxs-lookup"><span data-stu-id="d252a-163">The CDMP Baseline Algorithms</span></span>](#the-cdmp-baseline-algorithms)
    -   [<span data-ttu-id="d252a-164">CRT-Gerätemodell-Baseline</span><span class="sxs-lookup"><span data-stu-id="d252a-164">CRT Device Model Baseline</span></span>](#crt-device-model-baseline)
    -   [<span data-ttu-id="d252a-165">Baseline für das LCD-Gerätemodell</span><span class="sxs-lookup"><span data-stu-id="d252a-165">LCD Device Model Baseline</span></span>](#lcd-device-model-baseline)
    -   [<span data-ttu-id="d252a-166">Basislinie des RGB-Drucker Geräte Modells</span><span class="sxs-lookup"><span data-stu-id="d252a-166">RGB Printer Device Model Baseline</span></span>](#rgb-printer-device-model-baseline)
    -   [<span data-ttu-id="d252a-167">Grundlegende Konfiguration des virtuellen Geräte Modells</span><span class="sxs-lookup"><span data-stu-id="d252a-167">RGB Virtual Device Model Baseline</span></span>](#rgb-virtual-device-model-baseline)
    -   [<span data-ttu-id="d252a-168">Baseline des CMYK-Drucker Geräte Modells</span><span class="sxs-lookup"><span data-stu-id="d252a-168">CMYK Printer Device Model Baseline</span></span>](#cmyk-printer-device-model-baseline)
    -   [<span data-ttu-id="d252a-169">Basislinie des RGB-projektorgeräts</span><span class="sxs-lookup"><span data-stu-id="d252a-169">RGB Projector Device Model Baseline</span></span>](#rgb-projector-device-model-baseline)
    -   [<span data-ttu-id="d252a-170">Basislinie des Modells für das Modell</span><span class="sxs-lookup"><span data-stu-id="d252a-170">ICC Device Model Baseline</span></span>](#icc-device-model-baseline)
-   [<span data-ttu-id="d252a-171">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d252a-171">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="d252a-172">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d252a-172">Overview</span></span>

<span data-ttu-id="d252a-173">Dieses Schema wird verwendet, um den Inhalt eines Farb Gerätemodell Profils (CDMP) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d252a-173">This schema is used to specify the content of a color device model profile(CDMP).</span></span> <span data-ttu-id="d252a-174">Die zugeordneten Basis Linien Algorithmen werden nachfolgend beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d252a-174">The associated baseline algorithms are described below.</span></span>

<span data-ttu-id="d252a-175">Das grundlegende Gerätemodell Profil-Schema (DMP) besteht aus den Stichproben Messungs Daten.</span><span class="sxs-lookup"><span data-stu-id="d252a-175">The basic device model profile (DMP) schema consists of the sampling measurement data.</span></span>

<span data-ttu-id="d252a-176">Die Stichproben Komponente des DMP-XML-Schemas bietet Unterstützung für grundlegende farbmessungs Ziele und konzentriert sich auf allgemeine Standard Ziele und Ziele, die für die Basisgeräte Modelle optimiert sind.</span><span class="sxs-lookup"><span data-stu-id="d252a-176">The sampling component of the DMP XML schema provides support for basic color measurement targets, focusing on common standard targets and targets optimized for the baseline device models.</span></span>

<span data-ttu-id="d252a-177">Darüber hinaus stellt das Geräte Profil spezifische Informationen zum Zielgeräte Modell bereit und stellt eine Richtlinie bereit, die vom baselinefallback-Gerätemodell verwendet werden kann, wenn das Zielmodell nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d252a-177">In addition, the device profile provides specific information on the targeted device model and provides a policy that the baseline fallback device model can use if the targeted model is unavailable.</span></span> <span data-ttu-id="d252a-178">Die Profil Instanzen können private Erweiterungen mit XML-Standard Erweiterungs Mechanismen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d252a-178">The profile instances can include private extensions using standard XML extension mechanisms.</span></span>

## <a name="color-device-model-profile-architecture"></a><span data-ttu-id="d252a-179">Architektur des Farb Gerätemodell Profils</span><span class="sxs-lookup"><span data-stu-id="d252a-179">Color Device Model Profile Architecture</span></span>

![Diagramm, in dem die Informationen angezeigt werden, die ein Gerätemodell Profil bilden.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a><span data-ttu-id="d252a-181">Das CDMP-Schema</span><span class="sxs-lookup"><span data-stu-id="d252a-181">The CDMP Schema</span></span>


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



## <a name="wcs-cdmp-v20-calibration-addition"></a><span data-ttu-id="d252a-182">WCS CDMP v 2.0-Kalibrierungs Addition</span><span class="sxs-lookup"><span data-stu-id="d252a-182">WCS CDMP v2.0 Calibration Addition</span></span>

<span data-ttu-id="d252a-183">Das **colordevicemodel** -Element des CDMP-Schemas wurde in Windows 7 aktualisiert, um das neue Kalibrierungs Element einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d252a-183">The **ColorDeviceModel** element of the CDMP schema has been updated in Windows 7 to include the new calibration element.</span></span> <span data-ttu-id="d252a-184">Das folgende Beispiel zeigt die Änderung des CDMP-Schemas.</span><span class="sxs-lookup"><span data-stu-id="d252a-184">The following shows the change to the CDMP schema.</span></span>


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



## <a name="the-cdmp-schema-elements"></a><span data-ttu-id="d252a-185">Die CDMP-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="d252a-185">The CDMP Schema Elements</span></span>

> [!Note]  
> <span data-ttu-id="d252a-186">Primäre Samplings sind primär Beispiele von rot, grün, blau, schwarz und weiß.</span><span class="sxs-lookup"><span data-stu-id="d252a-186">Primaries are primary samples of red, green, blue, black, and white.</span></span> <span data-ttu-id="d252a-187">Eine primäre Anlauf Linie ist eine klangliche Abweichung von der geringsten Helligkeit bis zum vollständigen primär Wert.</span><span class="sxs-lookup"><span data-stu-id="d252a-187">A primary ramp is a tonal ramp from least luminance to full primary value.</span></span> <span data-ttu-id="d252a-188">Die maximale Anzahl von Einträgen in einer tonampe beträgt 4096.</span><span class="sxs-lookup"><span data-stu-id="d252a-188">The maximum number of entries in a tone ramp is 4096.</span></span>

 

> [!Note]  
> <span data-ttu-id="d252a-189">Für DMPs sind Messungs Daten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d252a-189">DMPs are required to have measurement data.</span></span>

 

### <a name="colordevicemodelprofile"></a><span data-ttu-id="d252a-190">Colordevicemodelprofile</span><span class="sxs-lookup"><span data-stu-id="d252a-190">ColorDeviceModelProfile</span></span>

<span data-ttu-id="d252a-191">Dieses Element weist den Typ colordevicemodel auf.</span><span class="sxs-lookup"><span data-stu-id="d252a-191">This element is of type ColorDeviceModel.</span></span>

<span data-ttu-id="d252a-192">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="d252a-192">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="colordevicemodel"></a><span data-ttu-id="d252a-193">Colordevicemodel</span><span class="sxs-lookup"><span data-stu-id="d252a-193">ColorDeviceModel</span></span>

<span data-ttu-id="d252a-194">Dieses Element stellt eine Sequenz der folgenden unter Elemente dar.</span><span class="sxs-lookup"><span data-stu-id="d252a-194">This element is a sequence of the following sub-elements</span></span>

1.  <span data-ttu-id="d252a-195">Profilnamen Zeichenfolge,</span><span class="sxs-lookup"><span data-stu-id="d252a-195">ProfileName string,</span></span>
2.  <span data-ttu-id="d252a-196">optionale Beschreibungs Zeichenfolge,</span><span class="sxs-lookup"><span data-stu-id="d252a-196">optional Description string,</span></span>
3.  <span data-ttu-id="d252a-197">optionale Autor Zeichenfolge,</span><span class="sxs-lookup"><span data-stu-id="d252a-197">optional Author string,</span></span>
4.  <span data-ttu-id="d252a-198">optionale "bedinrementconditions", "bedinrementconditionstype",</span><span class="sxs-lookup"><span data-stu-id="d252a-198">optional MeasurementConditions MeasurementConditionsType,</span></span>
5.  <span data-ttu-id="d252a-199">Self-Luminous boolescher Wert,</span><span class="sxs-lookup"><span data-stu-id="d252a-199">Self-Luminous Boolean,</span></span>
6.  <span data-ttu-id="d252a-200">Maxcolorant float,</span><span class="sxs-lookup"><span data-stu-id="d252a-200">MaxColorant float,</span></span>
7.  <span data-ttu-id="d252a-201">Mincolorant float,</span><span class="sxs-lookup"><span data-stu-id="d252a-201">MinColorant float,</span></span>
8.  <span data-ttu-id="d252a-202">Auswahl von Elementen</span><span class="sxs-lookup"><span data-stu-id="d252a-202">Choice of elements</span></span>
    1.  <span data-ttu-id="d252a-203">Crtdevice,</span><span class="sxs-lookup"><span data-stu-id="d252a-203">CRTDevice,</span></span>
    2.  <span data-ttu-id="d252a-204">Lcddevice,</span><span class="sxs-lookup"><span data-stu-id="d252a-204">LCDDevice,</span></span>
    3.  <span data-ttu-id="d252a-205">Rgbprojector Device,</span><span class="sxs-lookup"><span data-stu-id="d252a-205">RGBProjectorDevice,</span></span>
    4.  <span data-ttu-id="d252a-206">Scannerdevice,</span><span class="sxs-lookup"><span data-stu-id="d252a-206">ScannerDevice,</span></span>
    5.  <span data-ttu-id="d252a-207">Cameradevice,</span><span class="sxs-lookup"><span data-stu-id="d252a-207">CameraDevice,</span></span>
    6.  <span data-ttu-id="d252a-208">Rgbprinterdevice,</span><span class="sxs-lookup"><span data-stu-id="d252a-208">RGBPrinterDevice,</span></span>
    7.  <span data-ttu-id="d252a-209">Cmykprinterdevice,</span><span class="sxs-lookup"><span data-stu-id="d252a-209">CMYKPrinterDevice,</span></span>
    8.  <span data-ttu-id="d252a-210">Rgbvirtualdevice,</span><span class="sxs-lookup"><span data-stu-id="d252a-210">RGBVirtualDevice,</span></span>
9.  <span data-ttu-id="d252a-211">Plugindevice,</span><span class="sxs-lookup"><span data-stu-id="d252a-211">PlugInDevice,</span></span>
10. <span data-ttu-id="d252a-212">Optionaler Erweiterungstyp für Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="d252a-212">optional Extension ExtensionType</span></span>

<span data-ttu-id="d252a-213">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="d252a-213">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="d252a-214">Zeichen folgen-unter Elemente können maximal 10.000 Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d252a-214">String sub-elements have a maximum of 10,000 characters.</span></span> <span data-ttu-id="d252a-215">Das maxcolorant-Unterelement muss größer oder gleich 0 (null) und größer als das mincolorant-Unterelement sein.</span><span class="sxs-lookup"><span data-stu-id="d252a-215">The MaxColorant sub-element must be greater than or equal to zero (0) and greater than the MinColorant sub-element.</span></span> <span data-ttu-id="d252a-216">Mincolorant kann negativ sein.</span><span class="sxs-lookup"><span data-stu-id="d252a-216">The MinColorant can be negative.</span></span>

### <a name="namespaceversion"></a><span data-ttu-id="d252a-217">Namespaceversion</span><span class="sxs-lookup"><span data-stu-id="d252a-217">NamespaceVersion</span></span>

<span data-ttu-id="d252a-218">xmlns: CDM = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="d252a-218">xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

<span data-ttu-id="d252a-219">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="d252a-219">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

### <a name="version"></a><span data-ttu-id="d252a-220">Version</span><span class="sxs-lookup"><span data-stu-id="d252a-220">Version</span></span>

<span data-ttu-id="d252a-221">Version = "1,0" mit Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d252a-221">Version = "1.0" with Windows Vista.</span></span>

<span data-ttu-id="d252a-222">Überprüfungs **Bedingungen:** Jeder Versions Wert &gt; 0,1 oder &lt; = 2,0 ist gültig, um nicht unterbrechende Änderungen im Format zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d252a-222">**Validation conditions:** Any version value &gt;0.1 or &lt;=2.0 is valid to support non-breaking changes to the format.</span></span>

### <a name="documentation"></a><span data-ttu-id="d252a-223">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d252a-223">Documentation</span></span>

<span data-ttu-id="d252a-224">Gerätemodell Profil-Schema.</span><span class="sxs-lookup"><span data-stu-id="d252a-224">Device Model Profile schema.</span></span>

<span data-ttu-id="d252a-225">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d252a-225">Copyright (C) Microsoft.</span></span> <span data-ttu-id="d252a-226">Alle Rechte vorbehalten.</span><span class="sxs-lookup"><span data-stu-id="d252a-226">All rights reserved.</span></span>

### <a name="crtdevice-element"></a><span data-ttu-id="d252a-227">Crtdevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-227">CRTDevice element</span></span>

<span data-ttu-id="d252a-228">Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines ".</span><span class="sxs-lookup"><span data-stu-id="d252a-228">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="d252a-229">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="d252a-229">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="lcddevice-element"></a><span data-ttu-id="d252a-230">Lcddevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-230">LCDDevice element</span></span>

<span data-ttu-id="d252a-231">Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines ".</span><span class="sxs-lookup"><span data-stu-id="d252a-231">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="d252a-232">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="d252a-232">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="projectordevice-element"></a><span data-ttu-id="d252a-233">Projector Device-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-233">ProjectorDevice element</span></span>

<span data-ttu-id="d252a-234">Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines "festgelegten" "" "" "".</span><span class="sxs-lookup"><span data-stu-id="d252a-234">This element is a sequence of sub-elements of a MeasurementData RGBProjectorMeasurementType.</span></span>

<span data-ttu-id="d252a-235">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="d252a-235">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="scannerdevice-element"></a><span data-ttu-id="d252a-236">Scannerdevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-236">ScannerDevice element</span></span>

<span data-ttu-id="d252a-237">Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines "festgelegten"-rgbcapturemessrementtype.</span><span class="sxs-lookup"><span data-stu-id="d252a-237">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="d252a-238">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="d252a-238">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cameradevice-element"></a><span data-ttu-id="d252a-239">Cameradevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-239">CameraDevice element</span></span>

<span data-ttu-id="d252a-240">Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines "festgelegten"-rgbcapturemessrementtype.</span><span class="sxs-lookup"><span data-stu-id="d252a-240">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="d252a-241">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="d252a-241">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbprinterdevice-element"></a><span data-ttu-id="d252a-242">Rgbprinterdevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-242">RGBPrinterDevice element</span></span>

<span data-ttu-id="d252a-243">Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines "festgelegten rgbprintermessrementtype".</span><span class="sxs-lookup"><span data-stu-id="d252a-243">This element is a sequence of sub-elements of a MeasurementData RGBPrinterMeasurementType.</span></span>

<span data-ttu-id="d252a-244">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="d252a-244">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cmykprinterdevice-element"></a><span data-ttu-id="d252a-245">Cmykprinterdevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-245">CMYKPrinterDevice element</span></span>

<span data-ttu-id="d252a-246">Bei diesem Element handelt es sich um eine Sequenz von unter Elementen eines festgelegten Elements "".</span><span class="sxs-lookup"><span data-stu-id="d252a-246">This element is a sequence of sub-elements of a MeasurementData CMYKPrinterMeasurementType.</span></span>

<span data-ttu-id="d252a-247">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="d252a-247">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbvirtualdevice-element"></a><span data-ttu-id="d252a-248">Rgbvirtualdevice-Element</span><span class="sxs-lookup"><span data-stu-id="d252a-248">RGBVirtualDevice element</span></span>

<span data-ttu-id="d252a-249">Dieses Element ist eine Sequenz von unter Elementen eines rgbvirtualmessrementdatatype.</span><span class="sxs-lookup"><span data-stu-id="d252a-249">This element is a sequence of sub-elements of a RGBVirtualMeasurementDataType.</span></span>

<span data-ttu-id="d252a-250">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="d252a-250">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="plugindevicetype"></a><span data-ttu-id="d252a-251">Pluginde vicetype</span><span class="sxs-lookup"><span data-stu-id="d252a-251">PlugInDeviceType</span></span>

<span data-ttu-id="d252a-252">Bei diesem Element handelt es sich um eine Sequenz eines GUID-guidtype und aller untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="d252a-252">This element is a sequence of a GUID GUIDType and any sub-elements.</span></span>

<span data-ttu-id="d252a-253">Überprüfungs **Bedingungen:** Die GUID wird verwendet, um die GUID der DM-Plug-in-dll zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d252a-253">**Validation conditions:** The GUID is used to match the DM PlugIn Dll GUID.</span></span> <span data-ttu-id="d252a-254">Es sind maximal 100.000 benutzerdefinierte unter Elemente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d252a-254">There are a maximum of 100,000 custom sub-elements.</span></span>

### <a name="rgbvirtualmeasurementtype"></a><span data-ttu-id="d252a-255">Rgbvirtualmessrementtype</span><span class="sxs-lookup"><span data-stu-id="d252a-255">RGBVirtualMeasurementType</span></span>

<span data-ttu-id="d252a-256">Dieses Element ist eine Sequenz, die aus</span><span class="sxs-lookup"><span data-stu-id="d252a-256">This element is a sequence consisting of</span></span>

1.  <span data-ttu-id="d252a-257">Rgbprimariesgroup-Gruppe</span><span class="sxs-lookup"><span data-stu-id="d252a-257">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="d252a-258">Eine Auswahl von</span><span class="sxs-lookup"><span data-stu-id="d252a-258">A choice of</span></span>
3.  -   <span data-ttu-id="d252a-259">Gamma</span><span class="sxs-lookup"><span data-stu-id="d252a-259">Gamma</span></span>
    -   <span data-ttu-id="d252a-260">Gammaoffsetgewinn</span><span class="sxs-lookup"><span data-stu-id="d252a-260">GammaOffsetGain</span></span>
    -   <span data-ttu-id="d252a-261">Gammaoffsetgainlineargam</span><span class="sxs-lookup"><span data-stu-id="d252a-261">GammaOffsetGainLinearGam</span></span>
    -   <span data-ttu-id="d252a-262">Toneresponsecurves-Elemente</span><span class="sxs-lookup"><span data-stu-id="d252a-262">ToneResponseCurves elements</span></span>

4.  <span data-ttu-id="d252a-263">optionale gamutboundarysamples gamutboundarysamplestype</span><span class="sxs-lookup"><span data-stu-id="d252a-263">optional GamutBoundarySamples GamutBoundarySamplesType</span></span>
5.  <span data-ttu-id="d252a-264">Timestamp-DateTime</span><span class="sxs-lookup"><span data-stu-id="d252a-264">TimeStamp dateTime</span></span>

<span data-ttu-id="d252a-265">Überprüfungs **Bedingungen:** Jedes untergeordnete Element dieser Typen verfügt über eigene Überprüfungs Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="d252a-265">**Validation conditions:** Each sub-element of these types has its own validation conditions.</span></span>

### <a name="gammatype"></a><span data-ttu-id="d252a-266">Gammatype</span><span class="sxs-lookup"><span data-stu-id="d252a-266">GammaType</span></span>

<span data-ttu-id="d252a-267">Dieses Element ist ein komplexer Typ, der aus dem-Attribut besteht.</span><span class="sxs-lookup"><span data-stu-id="d252a-267">This element is a complex type consisting of the attribute</span></span>

-   <span data-ttu-id="d252a-268">Gamma nonnegativefloattype</span><span class="sxs-lookup"><span data-stu-id="d252a-268">Gamma NonNegativeFloatType</span></span>

<span data-ttu-id="d252a-269">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-269">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgaintype"></a><span data-ttu-id="d252a-270">Gammaoffsetgaintype</span><span class="sxs-lookup"><span data-stu-id="d252a-270">GammaOffsetGainType</span></span>

<span data-ttu-id="d252a-271">Dieses Element ist ein komplexer Typ, der aus den Attributen besteht.</span><span class="sxs-lookup"><span data-stu-id="d252a-271">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="d252a-272">Gamma nonnegativefloattype</span><span class="sxs-lookup"><span data-stu-id="d252a-272">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="d252a-273">Offset nonnegativefloattype</span><span class="sxs-lookup"><span data-stu-id="d252a-273">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="d252a-274">Nonnegativefloattype gewinnen</span><span class="sxs-lookup"><span data-stu-id="d252a-274">Gain NonNegativeFloatType</span></span>

<span data-ttu-id="d252a-275">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-275">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgainlineargaintype"></a><span data-ttu-id="d252a-276">Gammaoffsetgainlineargaintype</span><span class="sxs-lookup"><span data-stu-id="d252a-276">GammaOffsetGainLinearGainType</span></span>

<span data-ttu-id="d252a-277">Dieses Element ist ein komplexer Typ, der aus den Attributen besteht.</span><span class="sxs-lookup"><span data-stu-id="d252a-277">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="d252a-278">Gamma nonnegativefloattype</span><span class="sxs-lookup"><span data-stu-id="d252a-278">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="d252a-279">Offset nonnegativefloattype</span><span class="sxs-lookup"><span data-stu-id="d252a-279">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="d252a-280">Nonnegativefloattype gewinnen</span><span class="sxs-lookup"><span data-stu-id="d252a-280">Gain NonNegativeFloatType</span></span>
-   <span data-ttu-id="d252a-281">Linear Gewinn nonnegativefloattype</span><span class="sxs-lookup"><span data-stu-id="d252a-281">LinearGain NonNegativeFloatType</span></span>
-   <span data-ttu-id="d252a-282">Transitionpoint nonnegativefloattype.</span><span class="sxs-lookup"><span data-stu-id="d252a-282">TransitionPoint NonNegativeFloatType.</span></span>

<span data-ttu-id="d252a-283">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-283">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="toneresponsecurvestype"></a><span data-ttu-id="d252a-284">Toneresponsecurvestype</span><span class="sxs-lookup"><span data-stu-id="d252a-284">ToneResponseCurvesType</span></span>

<span data-ttu-id="d252a-285">Dieses Element ist eine Sequenz von</span><span class="sxs-lookup"><span data-stu-id="d252a-285">This element is a sequence of</span></span>

1.  <span data-ttu-id="d252a-286">Redtrc floatpaarlist</span><span class="sxs-lookup"><span data-stu-id="d252a-286">RedTRC FloatPairList</span></span>
2.  <span data-ttu-id="d252a-287">Greentrc floatpaarlist</span><span class="sxs-lookup"><span data-stu-id="d252a-287">GreenTRC FloatPairList</span></span>
3.  <span data-ttu-id="d252a-288">Bluetrc floatpaarlist</span><span class="sxs-lookup"><span data-stu-id="d252a-288">BlueTRC FloatPairList</span></span>

<span data-ttu-id="d252a-289">Das-Element verfügt auch über ein Attribut vom Typ "unsignetdint".</span><span class="sxs-lookup"><span data-stu-id="d252a-289">The element also has an attribute TRCLength of unsignedint type.</span></span>

<span data-ttu-id="d252a-290">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-290">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gamutboundarysamplestype"></a><span data-ttu-id="d252a-291">Gamutboundarysamplestype</span><span class="sxs-lookup"><span data-stu-id="d252a-291">GamutBoundarySamplesType</span></span>

<span data-ttu-id="d252a-292">Dieses Element ist eine Sequenz von RGB rgbtypes.</span><span class="sxs-lookup"><span data-stu-id="d252a-292">This element is a sequence of RGB RGBTypes.</span></span>

<span data-ttu-id="d252a-293">Überprüfungs **Bedingungen:** Derzeit unbegrenzte Anzahl von vorkommen, die auf der Grundlage des Branchen Feedbacks begrenzt werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-293">**Validation conditions:** Currently unbounded maximum occurences, to be capped based on industry feedback.</span></span>

### <a name="floatpairlist"></a><span data-ttu-id="d252a-294">Floatpaarlist</span><span class="sxs-lookup"><span data-stu-id="d252a-294">FloatPairList</span></span>

<span data-ttu-id="d252a-295">Dieses Element ist ein einfacher Typ von Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="d252a-295">This element is a simple type of list of pairs of floats.</span></span>

<span data-ttu-id="d252a-296">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-296">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="cmykprintermeasurementtype"></a><span data-ttu-id="d252a-297">Cmykprintermessbare rementtype</span><span class="sxs-lookup"><span data-stu-id="d252a-297">CMYKPrinterMeasurementType</span></span>

<span data-ttu-id="d252a-298">Dieses Element ist ein</span><span class="sxs-lookup"><span data-stu-id="d252a-298">This element is a</span></span>

1. <span data-ttu-id="d252a-299">die Sequenz des colorcube-Elements, das aus einer Sequenz von Sample nonnegativecmyksampletype besteht.</span><span class="sxs-lookup"><span data-stu-id="d252a-299">sequence of ColorCube element consisting of a sequence of Sample NonNegativeCMYKSampleType</span></span>

2. <span data-ttu-id="d252a-300">Timestamp-DateTime-Attribut.</span><span class="sxs-lookup"><span data-stu-id="d252a-300">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="d252a-301">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-301">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprintermeasurementtype"></a><span data-ttu-id="d252a-302">Rgbprintermessbare rementtype</span><span class="sxs-lookup"><span data-stu-id="d252a-302">RGBPrinterMeasurementType</span></span>

<span data-ttu-id="d252a-303">Dieses Element ist ein</span><span class="sxs-lookup"><span data-stu-id="d252a-303">This element is a</span></span>

1. <span data-ttu-id="d252a-304">die Sequenz des colorcube-Elements, das aus einer Sequenz von Sample nonnegativergbsampletype besteht.</span><span class="sxs-lookup"><span data-stu-id="d252a-304">sequence of ColorCube element consisting of a sequence of Sample NonNegativeRGBSampleType</span></span>

2. <span data-ttu-id="d252a-305">Timestamp-DateTime-Attribut.</span><span class="sxs-lookup"><span data-stu-id="d252a-305">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="d252a-306">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-306">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbcapturemeasurementtype"></a><span data-ttu-id="d252a-307">Rgbcapturemessrementtype</span><span class="sxs-lookup"><span data-stu-id="d252a-307">RGBCaptureMeasurementType</span></span>

<span data-ttu-id="d252a-308">Dieses Element ist eine Sequenz von</span><span class="sxs-lookup"><span data-stu-id="d252a-308">This element is a sequence of</span></span>

1.  <span data-ttu-id="d252a-309">ComplexType für primaryindex von</span><span class="sxs-lookup"><span data-stu-id="d252a-309">PrimaryIndex complexType of</span></span>
2.  1.  <span data-ttu-id="d252a-310">Weiß onebasedindex</span><span class="sxs-lookup"><span data-stu-id="d252a-310">White OneBasedIndex</span></span>
    2.  <span data-ttu-id="d252a-311">Optionaler schwarzer onebasedindex</span><span class="sxs-lookup"><span data-stu-id="d252a-311">Optional Black OneBasedIndex</span></span>
    3.  <span data-ttu-id="d252a-312">Optionaler roter onebasedindex</span><span class="sxs-lookup"><span data-stu-id="d252a-312">Optional Red OneBasedIndex</span></span>
    4.  <span data-ttu-id="d252a-313">Optionales grünes onebasedindex</span><span class="sxs-lookup"><span data-stu-id="d252a-313">Optional Green OneBasedIndex</span></span>
    5.  <span data-ttu-id="d252a-314">Optionaler blauer onebasedindex</span><span class="sxs-lookup"><span data-stu-id="d252a-314">Optional Blue OneBasedIndex</span></span>
    6.  <span data-ttu-id="d252a-315">Optionales Cyan onebasedindex</span><span class="sxs-lookup"><span data-stu-id="d252a-315">Optional Cyan OneBasedIndex</span></span>
    7.  <span data-ttu-id="d252a-316">Optionaler onebasedindex (optional)</span><span class="sxs-lookup"><span data-stu-id="d252a-316">Optional Magenta OneBasedIndex</span></span>
    8.  <span data-ttu-id="d252a-317">Optionaler gelber onebasedindex</span><span class="sxs-lookup"><span data-stu-id="d252a-317">Optional Yellow OneBasedIndex</span></span>

3.  <span data-ttu-id="d252a-318">Neutralindizes von Linien von onebasedindex</span><span class="sxs-lookup"><span data-stu-id="d252a-318">NeutralIndices of lines of OneBasedIndex</span></span>
4.  <span data-ttu-id="d252a-319">Colorsamples-Sequenz von Sample nonnegativergbsampletype</span><span class="sxs-lookup"><span data-stu-id="d252a-319">ColorSamples sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="d252a-320">Das-Element verfügt auch über ein Timestamp-DateTime-Attribut.</span><span class="sxs-lookup"><span data-stu-id="d252a-320">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="d252a-321">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-321">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="onebasedindex"></a><span data-ttu-id="d252a-322">Onebasedindex</span><span class="sxs-lookup"><span data-stu-id="d252a-322">OneBasedIndex</span></span>

<span data-ttu-id="d252a-323">Dieses Element ist eine einfache Art von Einschränkungs Basis ohne Vorzeichen (int) mit minInclusive Value = "1".</span><span class="sxs-lookup"><span data-stu-id="d252a-323">This element is a simple type of restriction base unsigned int with minInclusive value = "1."</span></span>

<span data-ttu-id="d252a-324">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-324">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprojectormeasurementtype"></a><span data-ttu-id="d252a-325">Rgbprojector messrementtype</span><span class="sxs-lookup"><span data-stu-id="d252a-325">RGBProjectorMeasurementType</span></span>

<span data-ttu-id="d252a-326">Dieses Element ist eine Sequenz von</span><span class="sxs-lookup"><span data-stu-id="d252a-326">This element is a sequence of</span></span>

1.  <span data-ttu-id="d252a-327">Rgbprimariesgroup-Gruppe</span><span class="sxs-lookup"><span data-stu-id="d252a-327">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="d252a-328">Color Samples-Element, das aus einer Sequenz von Sample nonnegativergbsampletype besteht</span><span class="sxs-lookup"><span data-stu-id="d252a-328">element ColorSamples consisting of sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="d252a-329">Das-Element verfügt auch über ein Timestamp-DateTime-Attribut.</span><span class="sxs-lookup"><span data-stu-id="d252a-329">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="d252a-330">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-330">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="displaymeasurementtype"></a><span data-ttu-id="d252a-331">Displaymessrementtype</span><span class="sxs-lookup"><span data-stu-id="d252a-331">DisplayMeasurementType</span></span>

<span data-ttu-id="d252a-332">Dieses Element ist eine Sequenz von</span><span class="sxs-lookup"><span data-stu-id="d252a-332">This element is a sequence of</span></span>

1.  <span data-ttu-id="d252a-333">Gruppe "rgbprimariesgroup"</span><span class="sxs-lookup"><span data-stu-id="d252a-333">group RGBPrimariesGroup</span></span>
2.  <span data-ttu-id="d252a-334">Grayramp der Sequenz von Sample nonnegativergbtype</span><span class="sxs-lookup"><span data-stu-id="d252a-334">GrayRamp of sequence of Sample NonNegativeRGBType</span></span>
3.  <span data-ttu-id="d252a-335">Redramp der Sequenz von Sample nonnegativergbtype</span><span class="sxs-lookup"><span data-stu-id="d252a-335">RedRamp of sequence of Sample NonNegativeRGBType</span></span>
4.  <span data-ttu-id="d252a-336">Greenramp der Sequenz von Sample nonnegativergbtype</span><span class="sxs-lookup"><span data-stu-id="d252a-336">GreenRamp of sequence of Sample NonNegativeRGBType</span></span>
5.  <span data-ttu-id="d252a-337">Blueramp der Sequenz von Sample nonnegativergbtype</span><span class="sxs-lookup"><span data-stu-id="d252a-337">BlueRamp of sequence of Sample NonNegativeRGBType</span></span>

<span data-ttu-id="d252a-338">Das displaymessrementtype-Element weist auch ein Timestamp-DateTime-Attribut auf.</span><span class="sxs-lookup"><span data-stu-id="d252a-338">The DisplayMeasurementType element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="d252a-339">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-339">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="measurementconditionstype"></a><span data-ttu-id="d252a-340">Messrementconditionstype</span><span class="sxs-lookup"><span data-stu-id="d252a-340">MeasurementConditionsType</span></span>

<span data-ttu-id="d252a-341">Der Wert für "bedinrementconditionstype" ist eine Sequenz von unter Elementen, die Folgendes enthält:</span><span class="sxs-lookup"><span data-stu-id="d252a-341">The MeasurementConditionsType is a sequence of sub-elements that contains:</span></span>

1.  <span data-ttu-id="d252a-342">Zeichen folgen-Enumerationswert "CIEXYZ" für colorspace-Einschränkung</span><span class="sxs-lookup"><span data-stu-id="d252a-342">ColorSpace restricted string enumeration value of "CIEXYZ"</span></span>
2.  <span data-ttu-id="d252a-343">optionale Auswahl von "White Point nonnegativexyztype" oder "whitepointname String Enumeration of values, D65, A" oder F2</span><span class="sxs-lookup"><span data-stu-id="d252a-343">optional choice of WhitePoint NonNegativeXYZType or WhitePointName string enumeration of values D50, D65, A, or F2</span></span>
3.  <span data-ttu-id="d252a-344">Geometry-geometrytype</span><span class="sxs-lookup"><span data-stu-id="d252a-344">Geometry GeometryType</span></span>
4.  <span data-ttu-id="d252a-345">Aperturesize Integer in Millimeter</span><span class="sxs-lookup"><span data-stu-id="d252a-345">ApertureSize integer in millimeters</span></span>

<span data-ttu-id="d252a-346">Standardwerte:</span><span class="sxs-lookup"><span data-stu-id="d252a-346">Defaults are:</span></span>

1.  <span data-ttu-id="d252a-347">RGB-und CMYK-Drucker:</span><span class="sxs-lookup"><span data-stu-id="d252a-347">RGB and CMYK Printers:</span></span>
    1.  <span data-ttu-id="d252a-348">CIEXYZ-messrementspacetype</span><span class="sxs-lookup"><span data-stu-id="d252a-348">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="d252a-349">D50-whitepointvalue</span><span class="sxs-lookup"><span data-stu-id="d252a-349">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="d252a-350">0/45 geometrytype</span><span class="sxs-lookup"><span data-stu-id="d252a-350">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="d252a-351">10mm-aperturesize</span><span class="sxs-lookup"><span data-stu-id="d252a-351">10mm ApertureSize</span></span>
2.  <span data-ttu-id="d252a-352">Can</span><span class="sxs-lookup"><span data-stu-id="d252a-352">Scanners:</span></span>
    1.  <span data-ttu-id="d252a-353">CIEXYZ-messrementspacetype</span><span class="sxs-lookup"><span data-stu-id="d252a-353">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="d252a-354">D50-whitepointvalue</span><span class="sxs-lookup"><span data-stu-id="d252a-354">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="d252a-355">0/45 geometrytype</span><span class="sxs-lookup"><span data-stu-id="d252a-355">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="d252a-356">10mm-aperturesize</span><span class="sxs-lookup"><span data-stu-id="d252a-356">10mm ApertureSize</span></span>
3.  <span data-ttu-id="d252a-357">Zeigt ein virtuelles Gerät an:</span><span class="sxs-lookup"><span data-stu-id="d252a-357">Displays and RGB Virtual Device:</span></span>
    1.  <span data-ttu-id="d252a-358">CIEXYZ-messrementspacetype</span><span class="sxs-lookup"><span data-stu-id="d252a-358">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="d252a-359">D65-whitepointvalue</span><span class="sxs-lookup"><span data-stu-id="d252a-359">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="d252a-360">0/45 geometrytype</span><span class="sxs-lookup"><span data-stu-id="d252a-360">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="d252a-361">10mm-aperturesize</span><span class="sxs-lookup"><span data-stu-id="d252a-361">10mm ApertureSize</span></span>
4.  <span data-ttu-id="d252a-362">Blitzer</span><span class="sxs-lookup"><span data-stu-id="d252a-362">Cameras:</span></span>
    1.  <span data-ttu-id="d252a-363">CIEXYZ-messrementspacetype</span><span class="sxs-lookup"><span data-stu-id="d252a-363">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="d252a-364">D65-whitepointvalue</span><span class="sxs-lookup"><span data-stu-id="d252a-364">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="d252a-365">Direkter geometrytype</span><span class="sxs-lookup"><span data-stu-id="d252a-365">Direct GeometryType</span></span>
    4.  <span data-ttu-id="d252a-366">10mm-aperturesize</span><span class="sxs-lookup"><span data-stu-id="d252a-366">10mm ApertureSize</span></span>

<span data-ttu-id="d252a-367">Überprüfungs **Bedingungen:** Die Validierung jedes untergeordneten Elements wird durch Validierungs Bedingungen für diese unter Elemente bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d252a-367">**Validation conditions:** Validation of each sub-element is determined by validation conditions for those sub-elements.</span></span> <span data-ttu-id="d252a-368">Wenn ein untergeordnetes Element fehlt, wird der jeweilige Standardwert für den Geräte Modelltyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-368">If any sub-element is missing, the device model type specific default is used.</span></span>

### <a name="geometrytype"></a><span data-ttu-id="d252a-369">Geometrytype</span><span class="sxs-lookup"><span data-stu-id="d252a-369">GeometryType</span></span>

<span data-ttu-id="d252a-370">String</span><span class="sxs-lookup"><span data-stu-id="d252a-370">String</span></span>

<span data-ttu-id="d252a-371">Enumerationswerte:</span><span class="sxs-lookup"><span data-stu-id="d252a-371">Enumeration values:</span></span>

-   <span data-ttu-id="d252a-372">"0/45"</span><span class="sxs-lookup"><span data-stu-id="d252a-372">"0/45"</span></span>
-   <span data-ttu-id="d252a-373">"0/diffus"</span><span class="sxs-lookup"><span data-stu-id="d252a-373">"0/diffuse"</span></span>
-   <span data-ttu-id="d252a-374">"Diffuses/0"</span><span class="sxs-lookup"><span data-stu-id="d252a-374">"diffuse/0"</span></span>
-   <span data-ttu-id="d252a-375">Unmittelbaren</span><span class="sxs-lookup"><span data-stu-id="d252a-375">"Direct"</span></span>

<span data-ttu-id="d252a-376">Überprüfungs **Bedingungen:** Jeder Wert außer den aufgelisteten Enumerationswerten ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d252a-376">**Validation conditions:** Any value except the enumberation values listed is invalid.</span></span> <span data-ttu-id="d252a-377">Diese Informationen ändern das Baseline-Verarbeitungs Verhalten nicht.</span><span class="sxs-lookup"><span data-stu-id="d252a-377">This information will not change baseline processing behavior.</span></span>

### <a name="rgbprimariesgroup"></a><span data-ttu-id="d252a-378">Rgbprimariesgroup</span><span class="sxs-lookup"><span data-stu-id="d252a-378">RGBPrimariesGroup</span></span>

<span data-ttu-id="d252a-379">Dieses Element ist eine Sequenz von</span><span class="sxs-lookup"><span data-stu-id="d252a-379">This element is a sequence of</span></span>

1.  <span data-ttu-id="d252a-380">Whiteprimary nonnegativexyztype</span><span class="sxs-lookup"><span data-stu-id="d252a-380">WhitePrimary NonNegativeXYZType</span></span>
2.  <span data-ttu-id="d252a-381">Redprimary nonnegativexyztype</span><span class="sxs-lookup"><span data-stu-id="d252a-381">RedPrimary NonNegativeXYZType</span></span>
3.  <span data-ttu-id="d252a-382">Greenprimary nonnegativexyztype</span><span class="sxs-lookup"><span data-stu-id="d252a-382">GreenPrimary NonNegativeXYZType</span></span>
4.  <span data-ttu-id="d252a-383">Blueprimary nonnegativexyztype</span><span class="sxs-lookup"><span data-stu-id="d252a-383">BluePrimary NonNegativeXYZTYpe</span></span>
5.  <span data-ttu-id="d252a-384">Blackprimary nonnegativexyztype</span><span class="sxs-lookup"><span data-stu-id="d252a-384">BlackPrimary NonNegativeXYZType</span></span>

<span data-ttu-id="d252a-385">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-385">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyksampletype"></a><span data-ttu-id="d252a-386">Nonnegativecmyksampletype</span><span class="sxs-lookup"><span data-stu-id="d252a-386">NonNegativeCMYKSampleType</span></span>

<span data-ttu-id="d252a-387">Dieses Element ist eine Sequenz von</span><span class="sxs-lookup"><span data-stu-id="d252a-387">This element is a sequence of</span></span>

1.  <span data-ttu-id="d252a-388">CMYK nonnegativecmyktype</span><span class="sxs-lookup"><span data-stu-id="d252a-388">CMYK NonNegativeCMYKType</span></span>
2.  <span data-ttu-id="d252a-389">CIEXYZ nonnegativexyztype</span><span class="sxs-lookup"><span data-stu-id="d252a-389">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="d252a-390">Das Element verfügt auch über eine optionale attributtagzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d252a-390">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="d252a-391">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-391">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbsampletype"></a><span data-ttu-id="d252a-392">Nonnegativergbsampletype</span><span class="sxs-lookup"><span data-stu-id="d252a-392">NonNegativeRGBSampleType</span></span>

<span data-ttu-id="d252a-393">Dieses Element ist eine Sequenz von</span><span class="sxs-lookup"><span data-stu-id="d252a-393">This element is a sequence of</span></span>

1.  <span data-ttu-id="d252a-394">RGB nonnegativergbtype</span><span class="sxs-lookup"><span data-stu-id="d252a-394">RGB NonNegativeRGBType</span></span>
2.  <span data-ttu-id="d252a-395">CIEXYZ nonnegativexyztype</span><span class="sxs-lookup"><span data-stu-id="d252a-395">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="d252a-396">Das Element verfügt auch über eine optionale attributtagzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d252a-396">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="d252a-397">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-397">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyktype"></a><span data-ttu-id="d252a-398">Nonnegativecmyktype</span><span class="sxs-lookup"><span data-stu-id="d252a-398">NonNegativeCMYKType</span></span>

<span data-ttu-id="d252a-399">Dieses Element, das aus Attributen besteht.</span><span class="sxs-lookup"><span data-stu-id="d252a-399">This element consisting of attributes</span></span>

1.  <span data-ttu-id="d252a-400">C float</span><span class="sxs-lookup"><span data-stu-id="d252a-400">C float</span></span>
2.  <span data-ttu-id="d252a-401">M float</span><span class="sxs-lookup"><span data-stu-id="d252a-401">M float</span></span>
3.  <span data-ttu-id="d252a-402">Y float</span><span class="sxs-lookup"><span data-stu-id="d252a-402">Y float</span></span>
4.  <span data-ttu-id="d252a-403">K float</span><span class="sxs-lookup"><span data-stu-id="d252a-403">K float</span></span>

<span data-ttu-id="d252a-404">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-404">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbtype"></a><span data-ttu-id="d252a-405">Nonnegativergbtype</span><span class="sxs-lookup"><span data-stu-id="d252a-405">NonNegativeRGBType</span></span>

<span data-ttu-id="d252a-406">Dieses Element, das aus Attributen besteht.</span><span class="sxs-lookup"><span data-stu-id="d252a-406">This element consisting of attributes</span></span>

1.  <span data-ttu-id="d252a-407">R float</span><span class="sxs-lookup"><span data-stu-id="d252a-407">R float</span></span>
2.  <span data-ttu-id="d252a-408">G float</span><span class="sxs-lookup"><span data-stu-id="d252a-408">G float</span></span>
3.  <span data-ttu-id="d252a-409">B float</span><span class="sxs-lookup"><span data-stu-id="d252a-409">B float</span></span>

<span data-ttu-id="d252a-410">Überprüfungs **Bedingungen:** Die Bestimmung durch das Branchen Feedback.</span><span class="sxs-lookup"><span data-stu-id="d252a-410">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="extensiontype"></a><span data-ttu-id="d252a-411">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d252a-411">ExtensionType</span></span>

<span data-ttu-id="d252a-412">Das ExtensionType-Element ist eine Sequenz eines beliebigen untergeordneten Elementtyps und wird für proprietäre Informationen von nicht-Microsoft-Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-412">The ExtensionType element is a sequence of any sub-element type and is used for proprietary information from non-Microsoft applications.</span></span>

<span data-ttu-id="d252a-413">Überprüfungs **Bedingungen:** Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="d252a-413">**Validation conditions:** This element is optional.</span></span> <span data-ttu-id="d252a-414">Es können maximal 1000 Erweiterungs unter Elemente vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d252a-414">There can be a maximum of 1000 extension sub-elements.</span></span>

### <a name="nonnegativexyztype"></a><span data-ttu-id="d252a-415">Nonnegativexyztype</span><span class="sxs-lookup"><span data-stu-id="d252a-415">NonNegativeXYZType</span></span>

<span data-ttu-id="d252a-416">Das nonnegativexyztype-Element besteht aus nonnegativefloattype mit drei IEEE-Gleit Komma Elementen mit einfacher Genauigkeit namens "X", "Y" und "Z".</span><span class="sxs-lookup"><span data-stu-id="d252a-416">The NonNegativeXYZType element is composed of NonNegativeFloatType three single-precision IEEE floating-point elements named "X," "Y," and "Z."</span></span> <span data-ttu-id="d252a-417">Diese Werte sind auf die Maßwerte der DMP-profile beschränkt.</span><span class="sxs-lookup"><span data-stu-id="d252a-417">These values are limited to the DMP profiles measurement values.</span></span> <span data-ttu-id="d252a-418">Bei diesen Messungen kann es sich entweder um absolute (nicht relative) CIEXYZ 1931-reflektierte Werte oder absolute (nicht relative) CIEXYZ 1931 Direct-Werte (Transmissive) in den quadratischen Einheiten von Kerzen pro Meter handelt.</span><span class="sxs-lookup"><span data-stu-id="d252a-418">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="d252a-419">Überprüfungs **Bedingungen:** Nur reale Werte sind gültig, und negative CIEXYZ-Mess Werte sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="d252a-419">**Validation conditions:** Only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="d252a-420">Da es sich hierbei um absolute Werte handelt, können Werte größer als 1,0 f sein.</span><span class="sxs-lookup"><span data-stu-id="d252a-420">Because these are absolute values, values can be greater than 1.0f.</span></span> <span data-ttu-id="d252a-421">Ein angemessener Grenzwert für "X", "Y" oder "Z".</span><span class="sxs-lookup"><span data-stu-id="d252a-421">A reasonable limit for any "X," "Y," or "Z."</span></span> <span data-ttu-id="d252a-422">der Wert ist willkürlich auf 10000.0 f festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d252a-422">value is arbitrarily set to 10000.0f.</span></span>

### <a name="xyztype"></a><span data-ttu-id="d252a-423">Xyztype</span><span class="sxs-lookup"><span data-stu-id="d252a-423">XYZType</span></span>

<span data-ttu-id="d252a-424">Das xyztype-Element besteht aus drei IEEE-Gleit Komma Werten mit einfacher Genauigkeit: "X", "Y" und "Z".</span><span class="sxs-lookup"><span data-stu-id="d252a-424">The XYZType element is composed of three single-precision IEEE floating-point values: "X," "Y," and "Z."</span></span>

## <a name="the-cdmp-baseline-algorithms"></a><span data-ttu-id="d252a-425">Die CDMP-baselinealgorithmen</span><span class="sxs-lookup"><span data-stu-id="d252a-425">The CDMP Baseline Algorithms</span></span>

### <a name="crt-device-model-baseline"></a><span data-ttu-id="d252a-426">CRT-Gerätemodell-Baseline</span><span class="sxs-lookup"><span data-stu-id="d252a-426">CRT Device Model Baseline</span></span>

<span data-ttu-id="d252a-427">Um dieses Modell zu verstehen, müssen Sie sowohl den Charakterisierungs Prozess als auch die Geräte Modellierung in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="d252a-427">To understand this model, you must consider both the characterization process and the device modeling.</span></span> <span data-ttu-id="d252a-428">Im Charakterisierungs Prozess werden XYZ-Messungen zuerst für die Farben ausgeführt, die durch Ausfüllen des Anzeige Puffers eines CRT-Anzeige Geräts abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-428">In the characterization process, XYZ measurements are first performed on the colors obtained by filling the display buffer of a CRT display device.</span></span> <span data-ttu-id="d252a-429">In den folgenden Beispiel Werten werden gute Daten für das CRT-Basisgeräte Modell generiert:</span><span class="sxs-lookup"><span data-stu-id="d252a-429">The following example values will generate good data for the baseline CRT device model:</span></span>

<span data-ttu-id="d252a-430">Rot: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span><span class="sxs-lookup"><span data-stu-id="d252a-430">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="d252a-431">Grün: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span><span class="sxs-lookup"><span data-stu-id="d252a-431">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="d252a-432">Blau: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span><span class="sxs-lookup"><span data-stu-id="d252a-432">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="d252a-433">Neutrals: R = G = B = 0, 8, 16, 32, 64, 128, 192, 255</span><span class="sxs-lookup"><span data-stu-id="d252a-433">Neutrals: R = G= B = 0, 8, 16, 32, 64, 128, 192, 255</span></span>

<span data-ttu-id="d252a-434">Andere Inkremente als 15 und nichtlineare Inkremente können ebenfalls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-434">Increments other than 15 and nonlinear increments can also be used.</span></span> <span data-ttu-id="d252a-435">Alle roten, grünen, blauen und neutralen Rampen müssen mindestens drei Stichproben enthalten, es wird jedoch empfohlen, weitere Beispiele zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d252a-435">Each red, green, blue, and neutral ramp must contain at least three samples, but providing more samples is recommended.</span></span> <span data-ttu-id="d252a-436">Sie müssen Beispiele für pure rot, grün, blau, schwarz und weiß bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d252a-436">You must provide samples for pure red, green, blue, black, and white.</span></span> <span data-ttu-id="d252a-437">Die Beispiele müssen nicht gleichmäßig verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-437">The samples do not have to be uniformly spaced.</span></span>

<span data-ttu-id="d252a-438">Der Prozess der buildstimulmatrizen besteht aus zwei Schritten.</span><span class="sxs-lookup"><span data-stu-id="d252a-438">The process of building the tristimulus matrix consists of two steps.</span></span> <span data-ttu-id="d252a-439">Schätzen Sie zuerst den Wert von "Black Point XYZ" oder "FLARE".</span><span class="sxs-lookup"><span data-stu-id="d252a-439">First, estimate the black point XYZ value, or the flare.</span></span> <span data-ttu-id="d252a-440">Dieser Schritt basiert größtenteils auf der Arbeit von Berns \[ 3 \] mit einer leicht geänderten Zielfunktion für die nichtlineare Optimierung.</span><span class="sxs-lookup"><span data-stu-id="d252a-440">This step is based largely on work of Berns\[3\] with a slightly modified objective function for the nonlinear optimization.</span></span> <span data-ttu-id="d252a-441">Zweitens berechnen Sie die Matrix für die Auswert Erstellung basierend auf dem Ergebnis aus Schritt 1 und auch aus einer durchschnittlichen Berechnung für alle pro-Channel-Messungen, nicht nur für die maximale digitale Anzahl.</span><span class="sxs-lookup"><span data-stu-id="d252a-441">Second, calculate tristimulus matrix based on the result from step one and also from an averaging calculation on all of the per-channel measurements, not just the one for maximum digital count.</span></span>

<span data-ttu-id="d252a-442">Jeder dieser Schritte enthält ausführliche Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="d252a-442">Each of these steps contains detailed procedures.</span></span> <span data-ttu-id="d252a-443">Der Ausgangspunkt ist die Rampen (17 Schritte in unserem Beispiel) für jeden R-, G-und B-Kanal.</span><span class="sxs-lookup"><span data-stu-id="d252a-443">The starting point is the ramps (17 steps in our example) for each of R, G, and B channels.</span></span> <span data-ttu-id="d252a-444">Wenn die XYZ-Messungen auf der Chromaticity- *XY* -Ebene dargestellt werden, ist in Abbildung 1 eine typische Situation dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d252a-444">When the XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="d252a-445">In Schritt 1 wird ein Problem mit der nichtlinearen Optimierung gelöst, um den am besten geeigneten schwarzen Punkt zu finden, der die Abweichung in der Chromaticity als eine durchläuft, die auf den Kanälen R, G und B verläuft.</span><span class="sxs-lookup"><span data-stu-id="d252a-445">Step one consists of solving a nonlinear optimization problem to find the "best fit" black point that will minimize the drift in chromaticity as one traverses along the R, G, and B channels.</span></span> <span data-ttu-id="d252a-446">Basierend auf Berns \[ 3 \] wird ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>K</sub>* ) gesucht, die die folgende Zielfunktion minimiert:</span><span class="sxs-lookup"><span data-stu-id="d252a-446">Based on Berns\[3\], we seek ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ) that minimizes the following objective function:</span></span>

![Zeigt die Zielfunktion an, bei der SR, SG und SB der Satz von Datenpunkten in den Kanälen R, G und B entsprechen.](images/cdmp-formula1.png)

<span data-ttu-id="d252a-448">Dabei sind *s <sub>R</sub>*,*s <sub>G</sub>* und *s <sub>B</sub>* der Satz von Datenpunkten, die den Punkten in den Kanälen R, G und b entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d252a-448">where *S <sub>R</sub>*,*S <sub>G</sub>*, and *S<sub>B</sub>* are the set of data points corresponding to the points on the R, G, and B channels.</span></span> <span data-ttu-id="d252a-449">Definieren Sie für alle festgelegten *e* Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d252a-449">For any set *S*, define:</span></span>

![Zeigt eine Formel zum Definieren von festgelegten S an.](images/cdmp-formula2.png)

<span data-ttu-id="d252a-451">In der vorangehenden \|  \| ist s die Kardinalität von *s*, d. h. die Anzahl der Punkte in den festgelegten *s*. ![ Zeigt eine Formel für die Chromatizität eines Punkts an.](images/cdmp-formula3.png)</span><span class="sxs-lookup"><span data-stu-id="d252a-451">In the preceding, \| *S* \| is the cardinality of *S*, i.e., the number of points in the set *S*. ![Shows a formula for the chromaticity of a point.](images/cdmp-formula3.png)</span></span> <span data-ttu-id="d252a-452">Gibt an, dass die Chromaticity-Koordinaten des Punkts ![ eine formaula für einen Punkt anzeigt.](images/cdmp-formula4.png)</span><span class="sxs-lookup"><span data-stu-id="d252a-452">is the chromaticity coordinates of the point ![Shows a formaula for a point.](images/cdmp-formula4.png)</span></span> <span data-ttu-id="d252a-453">, ![ zeigt eine Formel für den Mittelwert oder Mittelpunkt der Masse ](images/cdmp-formula5.png) an., ist der Durchschnitt oder Mittelpunkt der Masse aller Punkte in den festgelegten *S* auf der Ebene der Chromaticity.</span><span class="sxs-lookup"><span data-stu-id="d252a-453">, so ![Shows a formula for the average or center of mass.](images/cdmp-formula5.png), is the average, or center of mass, of all the points in the set *S* in the chromaticity plane.</span></span> <span data-ttu-id="d252a-454">Folglich ![ zeigt eine Formel für die Summe eines zweiten Zeitpunkts von Punkten an.](images/cdmp-formula6.png)</span><span class="sxs-lookup"><span data-stu-id="d252a-454">Thus, ![Shows a formula for the sum of a second moments of points.](images/cdmp-formula6.png)</span></span> <span data-ttu-id="d252a-455">ist die Summe aus den zweiten Augenblicken in Bezug auf den Mittelpunkt der Masse und ist ein Maß dafür, wie die Punkte verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-455">is the sum of second moments of the points about the center of mass and is a measure of how spread out the points are about it.</span></span> <span data-ttu-id="d252a-456">Schließlich wird ![ eine Formel für das Gesamt Measure der Verteilung von drei Clustern von Punkten angezeigt.](images/cdmp-formula7.png)</span><span class="sxs-lookup"><span data-stu-id="d252a-456">Finally, ![Shows a formula for the total measure of the spread of three clusters of points.](images/cdmp-formula7.png)</span></span> <span data-ttu-id="d252a-457">ist ein Gesamt Measure der Verteilung der drei Cluster Punkte auf die jeweiligen Mittelpunkte.</span><span class="sxs-lookup"><span data-stu-id="d252a-457">is a total measure of how spread out the three clusters of points are about their respective centers of mass.</span></span>

<span data-ttu-id="d252a-458">In der Berechnung von wird ![ eine Formel von f (X, Y, Z;) angezeigt. XK, YK, ZK).](images/cdmp-formula8.png)</span><span class="sxs-lookup"><span data-stu-id="d252a-458">In the calculation of ![Shows a formula of f(X,Y,Z; Xk, Yk, Zk).](images/cdmp-formula8.png)</span></span> <span data-ttu-id="d252a-459">Wenn ![ eine Formel für X. anzeigt ](images/cdmp-formula9.png) , wird die Berechnung übersprungen und die Kardinalität von *S* entsprechend angepasst.</span><span class="sxs-lookup"><span data-stu-id="d252a-459">, if ![Shows a formula for X.](images/cdmp-formula9.png) , then the calculation is skipped, and the cardinality of *S* is adjusted accordingly.</span></span>

<span data-ttu-id="d252a-460">Trotz der offensichtlichen Komplexität der Zielfunktion handelt es sich um eine Summe der Quadrate von vielen differenzierbaren Funktionen in *X <sub>K</sub>*,*Y <sub>k</sub>Z <sub>k</sub>* (17 Punkte 2 *XY* -Components 3 Channels = 102, im Beispiel) und ist daher für Standardverfahren für nichtlineare minimal Quadrate geeignet, wie z. b. den Levenberg-Marquardt Algorithmus, bei dem es sich um den in WCS verwendeten Algorithmus handelt.</span><span class="sxs-lookup"><span data-stu-id="d252a-460">Despite the apparent complexity of the objective function, it is a sum of the squares of many differentiable functions in *X <sub>K</sub>*,*Y <sub>K</sub>Z <sub>K</sub>* (17 points   2 *xy* -components   3 channels = 102, in the example), and, therefore, is amenable to standard nonlinear least squares techniques, such as the Levenberg-Marquardt algorithm, which is the algorithm used in WCS.</span></span> <span data-ttu-id="d252a-461">Beachten Sie, dass sich die vorangehende Zielfunktion von der in Berns 3 vorgeschlagenen unterscheidet, \[ \] dass die letztere Funktion die Varianz der Entfernungen vom Mittelpunkt der Masse misst, sodass die Varianz NULL ist, wenn die Punkte vom Mittelpunkt der Masse entfernt sind, auch wenn Sie vielleicht etwas darüber verteilt sind.</span><span class="sxs-lookup"><span data-stu-id="d252a-461">Note that the preceding objective function is different from the one suggested in Berns\[3\] in that the latter function measures the variance of the distances from the center of mass, so that the variance is zero when the points are equidistant from the center of mass, even though they may spread out quite a bit about it.</span></span> <span data-ttu-id="d252a-462">Im Beispiel wird die Verteilung von Punkten direkt mit den zweiten Augenblicken gesteuert.</span><span class="sxs-lookup"><span data-stu-id="d252a-462">In the example, the dispersion of points is contolled directly using the second moments.</span></span>

<span data-ttu-id="d252a-463">Wie bei jedem iterativen Algorithmus für das Problem bei nichtlinearen Quadraten erfordert Levenberg-Marquardt eine anfängliche Vermutung.</span><span class="sxs-lookup"><span data-stu-id="d252a-463">As with any iterative algorithm for the nonlinear least squares problem, Levenberg-Marquardt requires an initial guess.</span></span> <span data-ttu-id="d252a-464">Es gibt zwei offensichtliche Kandidaten.</span><span class="sxs-lookup"><span data-stu-id="d252a-464">There are two obvious candidates.</span></span> <span data-ttu-id="d252a-465">Eins ist (0,0); der andere ist der gemessene schwarze Punkt.</span><span class="sxs-lookup"><span data-stu-id="d252a-465">One is (0, 0, 0); the other is the measured black point.</span></span> <span data-ttu-id="d252a-466">Für den allgemeinen Tabellen Ausdruck wird der gemessene schwarze Punkt zuerst als erste Vermutung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-466">For the CTE, the measured black point is first used as the initial guess.</span></span> <span data-ttu-id="d252a-467">Wenn maximal 100 Iterationen überschritten werden, ohne dass ein Schwellenwert mit einer durchschnittlichen Entfernung von 0,001 der einzelnen Punkte von der Mitte der Masse erreicht wird (was einem Schwellenwert von (0,001) 17 3 = 0,000051 für die Zielfunktion entspricht), wird eine andere Runde von Iterationen mit der anfänglichen Vermutung (0, 0, 0) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d252a-467">If a maximum of 100 iterations is exceeded without achieving a threshold of an average distance of 0.001 of each point from its center of mass (which corresponds to a threshold value of (0.001)    17   3 = 0.000051 for the objective function), then another round of iterations with the initial guess of (0, 0, 0) is performed.</span></span> <span data-ttu-id="d252a-468">Die resultierende Schätzung des schwarzen Punkts ist XYZ, verglichen mit der besten Schätzung aus der vorherigen Runde der Iterationen (mit dem gemessenen schwarzen Punkt als anfängliche Vermutung).</span><span class="sxs-lookup"><span data-stu-id="d252a-468">The resulting estimate of the black point is XYZ compared with the best estimate from the previous round of iterations (with the measured black point as the initial guess).</span></span> <span data-ttu-id="d252a-469">Verwenden Sie die Schätzung, die den kleinsten Wert für die Zielfunktion liefert.</span><span class="sxs-lookup"><span data-stu-id="d252a-469">Use the estimate that gives the smallest value for the objective function.</span></span> <span data-ttu-id="d252a-470">Die Auswahl von 100 Iterationen und der Fehler Entfernung von 0,001 wurde jeweils empirisch ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d252a-470">The choice of 100 iterations and the error distance of 0.001 were each selected empirically.</span></span> <span data-ttu-id="d252a-471">In zukünftigen Versionen kann es sinnvoll sein, die Fehler Entfernung zu parametrisieren.</span><span class="sxs-lookup"><span data-stu-id="d252a-471">In future versions, it might be reasonable to parameterize the error distance.</span></span>

<span data-ttu-id="d252a-472">Das Ergebnis von Schritt 1 ist der geschätzte schwarze Punkt ( *X <sub>k</sub>*,*Y <sub>K</sub>*,*Z <sub>k</sub>* ).</span><span class="sxs-lookup"><span data-stu-id="d252a-472">The result of step one is the estimated black point ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ).</span></span> <span data-ttu-id="d252a-473">In Schritt 2 wird die Matrix mit den drei Stufen ermittelt, indem die Chromatizität der Punkte in den drei in Schritt 1 erhaltenen Clustern überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="d252a-473">Step two consists of determining the tristimulus matrix by averaging the chromaticity of the points in the three clusters obtained in step one.</span></span> <span data-ttu-id="d252a-474">Bei CRTs erfolgt dies in erster Linie, um die Auswirkungen von Messfehlern zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="d252a-474">For CRTs, this is done primarily to minimize the effects of measurement errors.</span></span> <span data-ttu-id="d252a-475">Die Punkte, die bei der Durchschnittsberechnung der Chromatizität verwendet werden, müssen die gleichen Punkte sein, die bei der Optimierung in Schritt 1 verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d252a-475">The points used in averaging the chromaticity must be the same points used in the optimization in step one.</span></span> <span data-ttu-id="d252a-476">Anders ausgedrückt: Wenn der erste Punkt (digitale Anzahl 15 im Beispiel) in jeder Rampe im Optimierungs Schritt verworfen wird, muss das gleiche im Mittelwert durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-476">In other words, if the first point (digital count 15, in the example) in each ramp is discarded in the optimization step, then the same must be done in the averaging.</span></span> <span data-ttu-id="d252a-477">, Wenn ![ Formeln der durchschnittlichen Chromatizität für Koordinaten in den roten und grünen Kanälen anzeigt.](images/cdmp-formula10.png)</span><span class="sxs-lookup"><span data-stu-id="d252a-477">If ![Shows formulas of averaged chromaticity for coordinates in the red and green channels.](images/cdmp-formula10.png)</span></span> <span data-ttu-id="d252a-478">und ![ zeigt eine Formel für den Mittelwert der-Koordinaten im blauen Kanal an.](images/cdmp-formula11.png)</span><span class="sxs-lookup"><span data-stu-id="d252a-478">, and ![Shows a formula of averaged chromaticity for coordinates in the blue channel.](images/cdmp-formula11.png)</span></span> <span data-ttu-id="d252a-479">Die Mittelwert Koordinaten der roten, grünen und blauen Kanäle werden im Mittelwert der folgenden Prozedur festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d252a-479">are the averaged chromaticity coordinates of the red, green, and blue channels, then the following procedure determines the tristimulus matrix.</span></span> <span data-ttu-id="d252a-480">Lösen Sie zunächst das lineare 3? 3-System:</span><span class="sxs-lookup"><span data-stu-id="d252a-480">First, solve the 3?3 linear system:</span></span>

![Zeigt den ersten Teil des Verfahrens zum Lösen eines linearen 3? 3-Systems.](images/cdmp-formula12.png)

![Zeigt den zweiten Teil des linearen Systems 3? 3 an.](images/cdmp-formula13.gif)![Zeigen Sie den t-index "t" am Ende des zweiten Teils des linearen Systems 3? 3 an.](images/cdmp-formula14.gif)

<span data-ttu-id="d252a-484">*X <sub>w</sub>*,*Y <sub>w</sub>*,*Z <sub>W</sub>*</span><span class="sxs-lookup"><span data-stu-id="d252a-484">*X <sub>W</sub>*,*Y <sub>W</sub>*,*Z<sub>W</sub>*</span></span>

![Zeigt den letzten Teil des Verfahrens zum Lösen eines linearen 3? 3-Systems.](images/cdmp-formula15.png)

<span data-ttu-id="d252a-486">Nachdem die matrixaus der Matrix festgelegt wurde, folgt die Bestimmung von Tonkurven dem Standardansatz.</span><span class="sxs-lookup"><span data-stu-id="d252a-486">After the tristimulus matrix is determined, the determination of tone curves follows the standard approach.</span></span> <span data-ttu-id="d252a-487">Bei CRT-Anzeige wird davon ausgegangen, dass die einzelnen Kanäle dem "Gog"-Modell folgen:</span><span class="sxs-lookup"><span data-stu-id="d252a-487">For CRT displays, the individual channels are assumed to follow the "GOG" model:</span></span>

![Zeigt die Formel für das ' g O g '-Modell an.](images/cdmp-formula16.png)

<span data-ttu-id="d252a-489">Dabei steht *k <sub>g</sub>* für den "Gewinn", 1-*k <sub>g</sub>* für den "Offset" und?</span><span class="sxs-lookup"><span data-stu-id="d252a-489">where *k <sub>g</sub>* is the "gain",1 -*k<sub>g</sub>* is the "offset", and ?</span></span> <span data-ttu-id="d252a-490">ist das "Gamma".</span><span class="sxs-lookup"><span data-stu-id="d252a-490">is the "gamma."</span></span> <span data-ttu-id="d252a-491">Die umgekehrte Matrix der Matrix mit den drei Werten wird auf die XYZ-Daten der neutrale angewendet, um die linearen RGB-Daten abzurufen, die dann mit den digitalen RGB-Werten korreliert werden, indem eine nichtlineare Regression für das Gog-Modell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d252a-491">The inverse matrix of the tristimulus matrix is applied to the XYZ data of the neutrals to obtain the linear RGB data, which is then correlated with the digital RGB values using nonlinear regression on the GOG model.</span></span> <span data-ttu-id="d252a-492">Diese Merkmale müssen nicht für die R-, G-und B-Kanäle identisch sein und sind im Allgemeinen nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="d252a-492">These characteristics do not have to be the same for the R, G, and B channels, and generally are not the same.</span></span>

<span data-ttu-id="d252a-493">Berns \[ 1 \] : Berns, *Abrechnungs-und Saltzman-Prinzipien der Farb Technologie*, 3 <sub>.</sub> d.</span><span class="sxs-lookup"><span data-stu-id="d252a-493">Berns\[1\]: Berns, *Billmeyer and Saltzman's Principles of Color Technology*, 3 <sub>rd</sub> Ed.</span></span> <span data-ttu-id="d252a-494">John Wiley & Sons (2000).</span><span class="sxs-lookup"><span data-stu-id="d252a-494">John Wiley & Sons (2000).</span></span>

<span data-ttu-id="d252a-495">Berns \[ 2 \] : Berns und Katoh, die digitale zu radiometrische Übertragungsfunktion für computergesteuerte CRT-Anzeige, das *Cie-Expertensymposium "97 Color Standards for Imaging Technology*, Nov. 1997.</span><span class="sxs-lookup"><span data-stu-id="d252a-495">Berns\[2\]: Berns and Katoh, The digital to radiometric transfer function for computer controlled CRT displays, *CIE Expert Symposium '97 Colour Standards for Imaging Technology*, Nov. 1997.</span></span>

<span data-ttu-id="d252a-496">Berns \[ 3 \] : Berns, Fernandez und Taplin, schätzen der Black-Level Computer-Controlled anzeigen, *Farb Recherche und Anwendung*, 28:379-383 Wiley-Zeitschriften, Inc. (2003)</span><span class="sxs-lookup"><span data-stu-id="d252a-496">Berns\[3\]: Berns, Fernandez and Taplin, Estimating Black-Level Emissions of Computer-Controlled Displays, *Color Research and Application*, 28: 379-383 Wiley Periodicals, Inc. (2003)</span></span>

<span data-ttu-id="d252a-497">Kang \[ 1 \] : Kang, *Farb Technologie für elektronische Imaging-Geräte*, spie (1997)</span><span class="sxs-lookup"><span data-stu-id="d252a-497">Kang\[1\]: Kang, *Color Technology for Electronic Imaging Devices*, SPIE (1997)</span></span>

<span data-ttu-id="d252a-498">Katoh \[ 1 \] : Katoh, Deguchi und Berns, eine genaue Charakterisierung des CRT-Monitor-Vorschlags (II) für eine Erweiterung der Cie-Methode und deren Verifizierung, *Opt. Rev.* 8:397-408 (2001)</span><span class="sxs-lookup"><span data-stu-id="d252a-498">Katoh\[1\]: Katoh, Deguchi and Berns, An accurate characterization of CRT monitor (II) proposal for an extension to CIE method and its verification, *Opt. Rev.* 8: 397-408 (2001)</span></span>

### <a name="lcd-device-model-baseline"></a><span data-ttu-id="d252a-499">Baseline für das LCD-Gerätemodell</span><span class="sxs-lookup"><span data-stu-id="d252a-499">LCD Device Model Baseline</span></span>

<span data-ttu-id="d252a-500">Die Basislinie für das LCD-Gerätemodell ähnelt der Basislinie des CRT-Geräte Modells.</span><span class="sxs-lookup"><span data-stu-id="d252a-500">The LCD Device Model Baseline is similar to the CRT Device Model Baseline.</span></span> <span data-ttu-id="d252a-501">In diesem Abschnitt wird erläutert, wie sich die LCD-Modellierung von der CRT-Modellierung unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="d252a-501">This section will explain the ways in which LCD modeling differs from CRT modeling.</span></span>

<span data-ttu-id="d252a-502">Ein Unterschied besteht darin, dass Sie nicht davon ausgehen können, dass die LCD-Anzeige dem für CRTs verwendeten Gog-Modell folgt und die audiokurven durch Interpolationen der gemessenen Daten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-502">One difference is that you cannot assume that LCD displays follow the GOG model used for CRTs, and the tone curves are obtained by interpolation of measured data.</span></span> <span data-ttu-id="d252a-503">Aus diesem Grund sollte die Geräte neutrale Achse häufiger getestet werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-503">Because of that, the device neutral axis should be sampled more frequently.</span></span>

<span data-ttu-id="d252a-504">Im folgenden finden Sie einige typische Beispiel Werte, die gute Daten für die Basislinie für das LCD-Gerätemodell generieren können:</span><span class="sxs-lookup"><span data-stu-id="d252a-504">Here are some typical example values that can generate good data for the LCD device model baseline:</span></span>

<span data-ttu-id="d252a-505">Rot: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span><span class="sxs-lookup"><span data-stu-id="d252a-505">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="d252a-506">Grün: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span><span class="sxs-lookup"><span data-stu-id="d252a-506">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="d252a-507">Blau: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span><span class="sxs-lookup"><span data-stu-id="d252a-507">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="d252a-508">Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span><span class="sxs-lookup"><span data-stu-id="d252a-508">Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span></span>

<span data-ttu-id="d252a-509">Der Prozess der Mittelwert Messung gemessener Farbwerte zum Abrufen der chromatitäten für die Geräte Replikate ist für LCDs kritischer als bei CRTs.</span><span class="sxs-lookup"><span data-stu-id="d252a-509">The process of averaging measured color chromaticies to obtain the chromaticities for the device primaries is more critical for LCDs than it is for CRTs.</span></span> <span data-ttu-id="d252a-510">Wenn XYZ-Messungen auf der Chromaticity- *XY* -Ebene dargestellt werden, ist in Abbildung 1 eine typische Situation dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d252a-510">When XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="d252a-511">Beachten Sie, dass sich die Chromaticity auf den schwarzen Punkt bewegt.</span><span class="sxs-lookup"><span data-stu-id="d252a-511">Notice how the chromaticity drifts toward the black point.</span></span> <span data-ttu-id="d252a-512">Dies liegt daran, dass alle LCDs über eine bestimmte Menge an leichten Lecks verfügen.</span><span class="sxs-lookup"><span data-stu-id="d252a-512">This is because all LCDs have a certain amount of light leakage.</span></span>

![Diagramm, das ein Diagramm der Chromatizität anzeigt, in dem Rohdaten ohne Korrektur verwendet werden.](images/cdmp-lcd-dmp-figure1.png)

<span data-ttu-id="d252a-514">**Abbildung 1** : das Chromaticity-Diagramm mit Rohdaten ohne Korrektur</span><span class="sxs-lookup"><span data-stu-id="d252a-514">**Figure 1** : The chromaticity diagram using raw data with no correction</span></span>

<span data-ttu-id="d252a-515">Wenn dies von den RAW-XYZ-Messungen subtrahiert wird, wird eine typische Situation in Abbildung 2 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d252a-515">When this is subtracted from the raw XYZ measurements, a typical situation is depicted in Figure 2.</span></span> <span data-ttu-id="d252a-516">Die Punkte sind nun auf drei Mittelpunkte gruppiert, auch wenn Sie nicht identisch sind.</span><span class="sxs-lookup"><span data-stu-id="d252a-516">Tthe points are now clustered about three centers, although they don't fall identically on them.</span></span> <span data-ttu-id="d252a-517">Der für CRTs beschriebene Durchschnitts Prozess verbessert die Ergebnisse für LCDs erheblich.</span><span class="sxs-lookup"><span data-stu-id="d252a-517">The averaging process described for CRTs greatly improves the results for LCDs.</span></span>

![Diagramm, das ein Diagramm der Chromatizität anzeigt, das Rohdaten mit einem angepassten schwarzen Punkt verwendet.](images/cdmp-lcd-dmp-figure2.png)

<span data-ttu-id="d252a-519">**Abbildung 2** : das Chromaticity-Diagramm mit Daten mit angepasstem Schwarzpunkt</span><span class="sxs-lookup"><span data-stu-id="d252a-519">**Figure 2** : The chromaticity diagram using data with adjusted black point</span></span>

### <a name="rgb-capture-device-model-baseline"></a><span data-ttu-id="d252a-520">RGB-Gerätemodell-Baseline erfassen</span><span class="sxs-lookup"><span data-stu-id="d252a-520">RGB Capture Device Model Baseline</span></span>

<span data-ttu-id="d252a-521">Das Basis Linien-RGB-Erfassungsgeräte Modell ist eine Unterklasse der idevicemodel-Klasse.</span><span class="sxs-lookup"><span data-stu-id="d252a-521">The baseline RGB capture device model is a subclass of the IDeviceModel class.</span></span> <span data-ttu-id="d252a-522">In der farbige Metrik-Charakterisierung von Farb Erfassungs Geräten, wie z. b. Scanner und Digitalkameras, wird die folgende Vorgehensweise verwendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-522">In the colorimetric characterization of color capture devices, such as scanners and digital cameras, the following approach is used.</span></span> <span data-ttu-id="d252a-523">Ein Ziel, das aus farbpatches mit bekannten CIEXYZ-Werten besteht, wird mit dem Erfassungsgerät erfasst.</span><span class="sxs-lookup"><span data-stu-id="d252a-523">A target consisting of color patches with known CIEXYZ values is captured using the capture device.</span></span> <span data-ttu-id="d252a-524">Das Ergebnis der Erfassung ist ein RGB-Bitmap-Bild, in dem die Farbe der einzelnen Patches in einem RGB-Wert codiert ist.</span><span class="sxs-lookup"><span data-stu-id="d252a-524">The result of the capture is an RGB bitmap image in which the color of each patch is encoded in an RGB value.</span></span> <span data-ttu-id="d252a-525">Diese Geräte RGB-Werte sind für ein bestimmtes Erfassungsgerät spezifisch.</span><span class="sxs-lookup"><span data-stu-id="d252a-525">These device RGB values are specific to a particular capture device.</span></span> <span data-ttu-id="d252a-526">Das Ziel der farbige Metrik-Charakterisierung besteht darin, eine empirische Beziehung zwischen den RGB-Werten des Geräts und den CIEXYZ-Werten herzustellen, oder eine mathematische Transformation zwischen RGB und XYZ, die das Verhalten des Aufzeichnungs Geräts so genau wie möglich modelliert.</span><span class="sxs-lookup"><span data-stu-id="d252a-526">The goal of colorimetric characterization is to establish an empirical relationship between the device RGB values and CIEXYZ values, or a mathematical transformation from RGB to XYZ that models as accurately as possible the behavior of the capture device.</span></span>

<span data-ttu-id="d252a-527">Eine solche mathematische Transformation kann in gewissem Maße durch Polynomen von niedrigem Grad modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-527">Such a mathematical transformation can be modeled reasonably by polynomials of low degrees.</span></span> <span data-ttu-id="d252a-528">Dieses Verfahren wird in der-Literatur ausführlich erläutert, z \[ . b. Kang 92 \] , Kang \[ 97 \] .</span><span class="sxs-lookup"><span data-stu-id="d252a-528">This procedure is detailed in the literature, for example Kang\[92\], Kang\[97\].</span></span> <span data-ttu-id="d252a-529">In Kang \[ 97 \] wird ein Ansatz berichtet, der einen Satz von drei polynomials mit 3, 6, 8, 9, 11, 14 oder 20 Begriffen in den Variablen R, G und B verwendet, während die drei Polynomen jeweils in die X-, Y-und Z-Komponenten des CIEXYZ-Raums fallen.</span><span class="sxs-lookup"><span data-stu-id="d252a-529">In Kang\[97\], an approach is reported that uses a set of three polynomials with 3, 6, 8, 9, 11, 14 or 20 terms in the R, G, and B variables, while the three polynomials regress respectively into the X, Y, Z components of the CIEXYZ space.</span></span> <span data-ttu-id="d252a-530">Für das 20-Term-polynomal lautet das Formular:</span><span class="sxs-lookup"><span data-stu-id="d252a-530">For the 20-term polynomial, the form is:</span></span>

![Zeigt die 20-Term polynomal an.](images/cdmp-formula20.png)

<span data-ttu-id="d252a-532">Es gibt ähnliche Ausdrücke für Y und Z. Das mathematische Verfahren für die Anpassung der Polynomen liegt innerhalb der "multivariate Linear Regression" und wird in jedem elementaren Text in der Statistik beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d252a-532">There are similar expressions for Y and Z. The mathematical technique for fitting the polynomials falls within "Multivariate Linear Regression" and is described in any elementary text in Statistics.</span></span>

<span data-ttu-id="d252a-533">Bei dieser Methode der linearen Regression wird die "Right"-Zielfunktion nicht minimiert.</span><span class="sxs-lookup"><span data-stu-id="d252a-533">This method of linear regression suffers from not minimizing the "right" objective function.</span></span> <span data-ttu-id="d252a-534">Entwurfs bedingt findet die lineare Regression die kleinste Quadrats Lösung. Dies impliziert, dass die erhaltenen Koeffizienten die Gesamtsumme der Quadrate von Fehlern im zugrunde liegenden Raum oder die Summe der Quadrate der euklidischen Entfernungen minimieren.</span><span class="sxs-lookup"><span data-stu-id="d252a-534">By design, linear regression finds the least squares solution, which implies that the coefficients obtained will minimize the total sum of squares of errors in the underlying space, or equivalently, the sum of squares of the Euclidean distances.</span></span> <span data-ttu-id="d252a-535">In der Praxis möchten Sie die Summe der Quadrate von minimieren? Es, wo? E ist einer der akzeptierten Standards, z. b. CIE94.</span><span class="sxs-lookup"><span data-stu-id="d252a-535">In practice, you want to minimize the sum of squares of ?Es, where ?E is one of the accepted standards such as CIE94.</span></span> <span data-ttu-id="d252a-536">Das minimieren dieser Zielfunktion ist ein nichtlineares Regressions Problem.</span><span class="sxs-lookup"><span data-stu-id="d252a-536">Minimizing this objective function is a nonlinear regression problem.</span></span>

<span data-ttu-id="d252a-537">In der neuen Engine ist Lab bis XYZ der CIE-Farbraum, der in zurückgezogen wird. das 20-jährige kubische polynomal wird als Modell für das Erfassungsgerät oder Koeffizienten ls, wie z. b., verwendet, so dass die folgenden Polynomen die Summe der Quadrate von minimieren? E <sub>CIE94</sub> s.</span><span class="sxs-lookup"><span data-stu-id="d252a-537">In the new engine, Lab to XYZ is the CIE color space that is regressed into, and the 20-term cubic polynomial is used as the model for the capture device, or coefficients ls,as,bs such that the following polynomials minimize the sum of squares of ?E <sub>CIE94</sub> s.</span></span>

![Zeigt eine Reihe von polynomialen Formeln an.](images/cdmp-formula21.png)

<span data-ttu-id="d252a-539">Die Lösung ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) im 60 dimensionalen echten numerischen Bereich **R** 203 muss so lauten, dass der folgende Gesamtfehler minimiert wird:</span><span class="sxs-lookup"><span data-stu-id="d252a-539">The solution ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) in the 60-dimensional real numeric space **R** 203 must be such that the following total error is minimized:</span></span>

![Zeigt den Gesamtfehler an, der minimiert werden soll.](images/cdmp-formula22.png)

<span data-ttu-id="d252a-541">wobei die sumzierung über alle Datenpunkt Paare erfolgt (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*).*L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* ) im DataSet mit Stichproben und zusätzliche Steuerungs Punkte, die in den folgenden Bereichen ausführlich erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-541">where the summation is through all the data point pairs (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v<sub>i</sub>* ) in the sampled data set plus additional control points to be detailed in the following.</span></span> <span data-ttu-id="d252a-542">Dies ist ein nichtlineares Regressions Problem, weil die Parameter *?<sub> i</sub>*, *a <sub>i</sub>*, \* <sub>i</sub>\* Eingabe in die Zielfunktion auf nichtlineare Weise (nicht quadratisch).</span><span class="sxs-lookup"><span data-stu-id="d252a-542">This is a nonlinear regression problem because the parameters *?<sub>i</sub>*, *a<sub>i</sub>*, \* <sub>i</sub>\* enter into the objective function in a nonlinear way (not quadratically).</span></span>

<span data-ttu-id="d252a-543">Da die Zielfunktion?</span><span class="sxs-lookup"><span data-stu-id="d252a-543">Because the objective function ?</span></span> <span data-ttu-id="d252a-544">ist eine nichtlineare (und nicht quadratische) Funktion der Parameter *?<sub> i</sub>*, *a <sub>i</sub>* und \* <sub>i</sub>\*, Sie müssen auf iterative Techniken zurückgreifen, um das Optimierungsproblem zu lösen.</span><span class="sxs-lookup"><span data-stu-id="d252a-544">is a nonlinear (and nonquadratic) function of the parameters *?<sub>i</sub>*, *a<sub>i</sub>* and \* <sub>i</sub>\*, you must resort to iterative techniques to solve the optimization problem.</span></span> <span data-ttu-id="d252a-545">Da es sich bei der Form der Zielfunktion um eine Summe von Quadraten handelt, wird eine standardmäßige Optimierungstechnik verwendet, die als Levenberg-Marquardt-Algorithmus bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d252a-545">Because the form of the objective function is a sum of squares, a standard optimization technique called the Levenberg-Marquardt algorithm is used.</span></span> <span data-ttu-id="d252a-546">Es wird als Methode der Wahl für nichtlineare, kleinste Quadrate behandelt.</span><span class="sxs-lookup"><span data-stu-id="d252a-546">It is considered the method of choice for nonlinear least squares problems.</span></span> <span data-ttu-id="d252a-547">Für iterative Algorithmen, wie z. b. Levenberg-Marquardt, müssen Sie eine anfängliche Vermutung angeben.</span><span class="sxs-lookup"><span data-stu-id="d252a-547">For iterative algorithms such as Levenberg-Marquardt, you must supply an initial guess.</span></span> <span data-ttu-id="d252a-548">Ein guter ursprünglicher Schätzwert ist normalerweise wichtig, um den richtigen Minimalwert zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="d252a-548">A good initial guess is usually critical in finding the correct minimum value.</span></span> <span data-ttu-id="d252a-549">In diesem Fall ist ein guter Kandidat für die anfängliche Schätzung die Lösung des linearen Regressions Problems.</span><span class="sxs-lookup"><span data-stu-id="d252a-549">In this case, one good candidate for the initial guess is the solution of the linear regression problem.</span></span> <span data-ttu-id="d252a-550">Minimieren Sie zunächst die Summe des Quadrats von euklidischen Entfernungen im Lab-Raum, indem Sie eine quadratische Zielfunktion definieren:</span><span class="sxs-lookup"><span data-stu-id="d252a-550">First, minimize the sum of the square of Euclidean distances in Lab space, by defining a quadratic objective function:</span></span>

![Zeigt eine definierte quadratische Zielfunktion an.](images/cdmp-formula23.png)

<span data-ttu-id="d252a-552">Die mathematische Lösung für das Problem "lineare geringste Quadrate" ist bekannt.</span><span class="sxs-lookup"><span data-stu-id="d252a-552">The mathematical solution to such "linear least squares" problem is well known.</span></span> <span data-ttu-id="d252a-553">Denn *?<sub> Ich</sub>* wird nur in der *L* -Modellierung angezeigt, *ein <sub>i</sub>* wird nur in der *u* -Modellierung angezeigt, und \* <sub>i</sub>\* wird nur in der *v* -Modellierung angezeigt. Das Optimierungsproblem kann in drei Unterprobleme zerlegt werden: eine für *L*, eine für *u* und eine für *v*.</span><span class="sxs-lookup"><span data-stu-id="d252a-553">Because *?<sub>i</sub>* only appears in the *L* modeling, *a <sub>i</sub>* only appears in the *u* modeling, and \* <sub>i</sub>\* only appears in the *v* modeling; the optimization problem can be decomposed into three subproblems: one for *L*, one for *u* and one for *v*.</span></span> <span data-ttu-id="d252a-554">Beachten Sie die *L* -Gleichungen.</span><span class="sxs-lookup"><span data-stu-id="d252a-554">Consider the *L* equations.</span></span> <span data-ttu-id="d252a-555">(Die *u* -Gleichungen und die *v* -Gleichungen folgen exakt dem gleichen Argument.) Das Problem der Minimierung der Summe der Fehler Quadrate in *L* kann als das Lösen der folgenden Matrix Gleichung in den geringsten Quadraten ausgedrückt werden:</span><span class="sxs-lookup"><span data-stu-id="d252a-555">(The *u* equations and the *v* equations follow exactly the same argument.) The problem of minimizing the sum of squares of errors in *L* can be stated as solving the following matrix equation in the least squares sense:</span></span>

![Zeigt eine Matrix Gleichung für L an.](images/cdmp-formula24.png)

<span data-ttu-id="d252a-557">Dabei steht *N* für die Gesamtanzahl der Datenpunkte (ursprüngliche Stichprobenpunkte Plus Steuerungs Punkte, die wie unten beschrieben erstellt werden).</span><span class="sxs-lookup"><span data-stu-id="d252a-557">where *N* is the total number of data points (original sampled points plus control points created in a manner described below).</span></span> <span data-ttu-id="d252a-558">Normalerweise ist *N* viel größer als 20, sodass die vorangehende Gleichung über gestellt wird, sodass eine kleinste Quadrats Lösung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d252a-558">Typically, *N* is much larger than 20, so the preceding equation is over-determined, requiring a least squares solution.</span></span> <span data-ttu-id="d252a-559">Eine geschlossene Formular Projekt Mappe für **?**</span><span class="sxs-lookup"><span data-stu-id="d252a-559">A closed form solution for **?**</span></span> <span data-ttu-id="d252a-560">verfügbar:</span><span class="sxs-lookup"><span data-stu-id="d252a-560">is available:</span></span>

![Zeigt eine geschlossene Formular Projekt Mappe an.](images/cdmp-formula25.png)

<span data-ttu-id="d252a-562">In der Praxis wird die direkte Auswertung mithilfe der geschlossenen Formular Lösung nicht verwendet, da Sie über schlechte numerische Eigenschaften verfügt.</span><span class="sxs-lookup"><span data-stu-id="d252a-562">In practice, direct evaluation using the closed form solution is not used because it has poor numerical properties.</span></span> <span data-ttu-id="d252a-563">Stattdessen wird ein beliebiger matrixfaktorisierungsalgorithmus auf die Koeffizienten-Matrix angewendet, wodurch das System der Gleichungen in eine kanonische Form reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="d252a-563">Instead, some kind of matrix factorization algorithm is applied to the coefficient matrix which reduces the system of equations to a canonical form.</span></span> <span data-ttu-id="d252a-564">In der aktuellen Implementierung wird die einmalige Wert Zerlegung (Single Value Zerlegung, SVD) auf die Matrix **R** angewendet, und dann wird das resultierende, zusammengesetzte System gelöst.</span><span class="sxs-lookup"><span data-stu-id="d252a-564">In the current implementation, Singular Value Decomposition (SVD) is applied to the matrix **R** and then the resulting decomposed system is solved.</span></span>

<span data-ttu-id="d252a-565">Die Lösung für das lineare Regressions Problem, das von angegeben wird, ![ zeigt die Lösung für das Problem der linearen Regression.](images/cdmp-formula26.png)</span><span class="sxs-lookup"><span data-stu-id="d252a-565">The solution to the linear regression problem, denoted by ![Shows the solution to the linear regression problem.](images/cdmp-formula26.png)</span></span> <span data-ttu-id="d252a-566">wird als Ausgangspunkt des Levenberg-Marquardt Algorithmus verwendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-566">, is used as the starting point of the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="d252a-567">In diesem Algorithmus wird ein Test Schritt berechnet, der den Punkt näher an die optimale Lösung verschieben sollte.</span><span class="sxs-lookup"><span data-stu-id="d252a-567">In this algorithm, a trial step is computed that should move the point closer to the optimal solution.</span></span> <span data-ttu-id="d252a-568">Der Test Schritt erfüllt einen Satz linearer Gleichungen, der vom funktionalen Wert und den Werten der Ableitungen am aktuellen Punkt abhängt.</span><span class="sxs-lookup"><span data-stu-id="d252a-568">The trial step satisfies a set of linear equations dependent on the functional value and values of the derivatives at the current point.</span></span> <span data-ttu-id="d252a-569">Aus diesem Grund sind die Ableitungen der Zielfunktion?</span><span class="sxs-lookup"><span data-stu-id="d252a-569">For this reason, the derivatives of the objective function ?</span></span> <span data-ttu-id="d252a-570">in Bezug auf die Parameter *?<sub> Ich</sub>* bin *für <sub></sub> <sub></sub>* den Levenberg-Marquardt Algorithmus Eingaben erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d252a-570">with respect to the parameters *?<sub>i</sub>*, *a<sub>i</sub> <sub>i</sub>* are required inputs to the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="d252a-571">Obwohl es 60 Parameter gibt, gibt es eine Verknüpfung, mit der Sie viel weniger berechnen können.</span><span class="sxs-lookup"><span data-stu-id="d252a-571">Although there are 60 parameters, there is a shortcut that allows you to compute a lot less.</span></span> <span data-ttu-id="d252a-572">Nach der Ketten Regel von "Kalkül"</span><span class="sxs-lookup"><span data-stu-id="d252a-572">By the Chain Rule of Calculus,</span></span>

![Zeigt eine Gleichung an, die eine Verknüpfung mithilfe der Ketten Regel von Kalkül zulässt.](images/cdmp-formula27.png)

<span data-ttu-id="d252a-574">Dabei ist *j* = 1, 2,, 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* der CIELAB-Wert des *i* Th-Beispiel Punkts, und *R <sub>IJ</sub>* ist der (*i*,*j* ) Th-Eintrag der oben definierten Matrix- **R** .</span><span class="sxs-lookup"><span data-stu-id="d252a-574">where *j* = 1, 2,  , 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* are the CIELAB value of the *i* th sample point, and *R <sub>ij</sub>* is the (*i*,*j* )th entry of the matrix **R** defined above.</span></span> <span data-ttu-id="d252a-575">Anstatt also Ableitungen für 60-Parameter zu berechnen, können Sie die Ableitungen für *L*,*a* und *b* mithilfe von numerischer vorwärts Differenzierung berechnen.</span><span class="sxs-lookup"><span data-stu-id="d252a-575">So instead of computing derivatives for 60 parameters, you can compute derivatives for *L*,*a*, and *b* using numerical forward differencing.</span></span>

<span data-ttu-id="d252a-576">Außerdem ist es erforderlich, ein Stopp Kriterium für iterative Algorithmen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="d252a-576">It is also necessary to set up a stopping criterion for iterative algorithms.</span></span> <span data-ttu-id="d252a-577">In der aktuellen Implementierung werden die Iterationen beendet, wenn das mittlere quadratische DECIE94 kleiner als 1 ist, oder wenn die Anzahl der durchgeführten Iterationen 10 überschritten hat.</span><span class="sxs-lookup"><span data-stu-id="d252a-577">In the current implementation, the iterations are terminated if the mean square DECIE94 is less than 1, or the number of iterations performed has exceeded 10.</span></span> <span data-ttu-id="d252a-578">Die Zahl 10 ergibt sich aus der Praxis, dass bei den ersten Iterationen, die den Fehler nicht signifikant verringern, weitere Iterationen nicht viel anderes unterstützen, als den Punkt in einer oszillatorischen Weise zu verschieben, d. h., der Algorithmus wird möglicherweise nicht konvergiert.</span><span class="sxs-lookup"><span data-stu-id="d252a-578">The number 10 comes from the practical experience that if the first few iterations do not reduce the error significantly, further iterations would not help much other than moving the point in an oscillatory manner, i.e., the algorithm may not converge.</span></span> <span data-ttu-id="d252a-579">Auch wenn der Algorithmus abweicht, können wir sicher sein, dass das DECIE94 nicht schlechter ist als das, was wir gestartet haben, d. h. mit den Parametern, die aus der linearen Regression abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="d252a-579">Even in the case that the algorithm diverges, we can be sure that the DECIE94 is no worse than what we started, i.e. with the parameters obtained from linear regression.</span></span>

<span data-ttu-id="d252a-580">Selbst bei der vorhergehenden Methode der nichtlinearen Regression gibt es mehrere Probleme bei der Anpassung.</span><span class="sxs-lookup"><span data-stu-id="d252a-580">Even with the preceding method of nonlinear regression, there are several problems with the fitting.</span></span> <span data-ttu-id="d252a-581">Ein Problem besteht darin, dass die Polynomen tendenziell über die Datenpunkte hinausgehen oder diese überschreiten.</span><span class="sxs-lookup"><span data-stu-id="d252a-581">One problem is that the polynomials tend to overshoot or undershoot beyond the data points.</span></span> <span data-ttu-id="d252a-582">Künstliche lokale Maximen und Mindestwerte können im Anpassungsprozess eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-582">Artificial local maxima and minima may be introduced in the fitting process.</span></span> <span data-ttu-id="d252a-583">Dies kann durch die Verwendung von polynomialen mit niedrigem Grad gegenseitig erfolgen. Dies ist der Grund, warum Sie nicht mehr als drei Grad verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="d252a-583">This can be counteracted by using polynomials of low degree, which is the reason you should not use higher than three degrees.</span></span> <span data-ttu-id="d252a-584">Ein schwerwiegenderer Aspekt der Überschreibung oder des Unterlaufs besteht darin, dass ein polynomal theoretisch einen beliebigen realen Wert annehmen kann, da der für die Modellierung verwendete Speicherplatz in der Regel über physische Einschränkungen und praktische Einschränkungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="d252a-584">A more serious aspect of overshooting or undershooting is that, while a polynomial can take any real value theoretically, the space it tries to model typically has physical constraints and practical constraints.</span></span> <span data-ttu-id="d252a-585">CIEXYZ muss alle X, Y, Z nicht negativ aufweisen, eine physische Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="d252a-585">CIEXYZ must have all of X, Y, Z non-negative, which is a physical constraint.</span></span> <span data-ttu-id="d252a-586">In der Praxis beanspruchen Sie nur Werte in der Größe von Hunderten, nicht Tausender oder höher.</span><span class="sxs-lookup"><span data-stu-id="d252a-586">In practice, they only take values in the magnitude of hundreds, not thousands or higher.</span></span> <span data-ttu-id="d252a-587">Ebenso hat CIELAB oder CIELUV eigene physische und praktische Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="d252a-587">Similarly, CIELAB or CIELUV has its own physical and practical constraints.</span></span> <span data-ttu-id="d252a-588">Wenn der RGB-Speicherplatz mit Beispiel Punkten ausreichend gefüllt ist, ist das Problem des über Schießens oder Unterlaufs nicht schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="d252a-588">When the RGB space is filled sufficiently with sample points, the problem of overshooting or undershooting is not serious.</span></span> <span data-ttu-id="d252a-589">Die erfassten RGB-Punkte vom Erfassungsgerät füllen den RGB-Speicherplatz jedoch in der Regel nicht gleichmäßig aus.</span><span class="sxs-lookup"><span data-stu-id="d252a-589">However, the captured RGB points from the capture device do not usually fill up the RGB space uniformly.</span></span> <span data-ttu-id="d252a-590">Die Punkte können nur innere 80% des RGB-Cubes auffüllen, oder Sie können sich in einem niedrigeren dimensionalen vielfachen befinden.</span><span class="sxs-lookup"><span data-stu-id="d252a-590">The points may fill up only inner the 80% of the RGB cube, or worse, they may reside in a lower dimensional manifold.</span></span> <span data-ttu-id="d252a-591">Wenn dies der Fall ist, können die zurück gestellten Polynomen einen schlechten Auftrag ausführen, um die Werte über die Datenpunkte hinaus zu extrapolieren. manchmal werden unrealistische Vorhersagen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d252a-591">When this happens, the regressed polynomials may do a poor job at extrapolating the values beyond the data points, sometimes returning unrealistic predictions.</span></span> <span data-ttu-id="d252a-592">Sie möchten ein Modell, das immer relativ realistische Werte zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d252a-592">You want a model that always returns reasonably realistic values.</span></span> <span data-ttu-id="d252a-593">Hierfür ist eine Methode erforderlich, mit der das Begrenzungs Verhalten von Regressions Polynomen effektiv gesteuert werden kann, indem den Polynomen, die sich in der Nähe der Grenze des RGB-Cubes befinden, zusätzliche Kosten entstehen.</span><span class="sxs-lookup"><span data-stu-id="d252a-593">This requires a method that can effectively control the boundary behavior of regression polynomials by imposing additional cost to those polynomials that behave erratically near the boundary of the RGB cube.</span></span> <span data-ttu-id="d252a-594">Ein weiteres Measure, mit dem sichergestellt wird, dass die Polynomen immer realistische Werte zurückgeben, wird durch Abschneiden der Ausgabe auf innerhalb des Cie-Spektral Lokus angewendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-594">A further measure to ensure that the polynomials always return realistic values is applied by clipping the output to within the CIE spectral locus.</span></span>

<span data-ttu-id="d252a-595">An diesem Punkt unterscheiden sich die scannermodellierung und die Kamera Modellierung voneinander.</span><span class="sxs-lookup"><span data-stu-id="d252a-595">It is at this point that the scanner modeling and camera modeling diverge from each other.</span></span> <span data-ttu-id="d252a-596">Es wird erwartet, dass das Kameramodell eine extrapolierte Region über die erfassten Punkte hinaus durchläuft, einschließlich der "Glanzlichter", die für das Scanner-Modell nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d252a-596">The camera model is expected to extrapolate to regions beyond the sampled points including the "specular highlights," the same extrapolation is not required for the scanner model.</span></span> <span data-ttu-id="d252a-597">Es wird erwartet, dass das scannerziel eine Ähnlichkeit abdeckt, die dem gedruckten Material ähnelt, das gescannt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d252a-597">The scanner target is expected to cover a characterization that is similar to the printed materials to be scanned.</span></span> <span data-ttu-id="d252a-598">Das Scanner-Modell muss in dem Sinne, dass es nicht unrealistische Werte zurückgeben sollte, immer noch robust sein, aber es ist nicht erforderlich, eine extra polierungs Version zu überschreiten.</span><span class="sxs-lookup"><span data-stu-id="d252a-598">The scanner model is still required to be robust in the sense that it should not return unrealistic values, but extrapolation far beyond the characterization target is not required.</span></span> <span data-ttu-id="d252a-599">Um die Stabilität sicherzustellen, wird die oben genannte L-Polynoms um 100 abgeschnitten, d. h., das polynomal wird gezwungen, nicht über "DMin" des scannerziels hinaus zu extrapolieren.</span><span class="sxs-lookup"><span data-stu-id="d252a-599">To ensure robustness, the L-polynomial above is clipped at 100, that is, the polynomial model is forced not to extrapolate beyond "Dmin" of the scanner target.</span></span>

<span data-ttu-id="d252a-600">Es wird erwartet, dass das Kameramodell zu Glanzlichtern extrapoliert, sodass Clipping bei 100 nicht erwünscht ist.</span><span class="sxs-lookup"><span data-stu-id="d252a-600">The camera model is expected to extrapolate to specular highlights, so clipping at 100 is undesirable.</span></span> <span data-ttu-id="d252a-601">Stattdessen wird der folgende Algorithmus verwendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-601">Instead, the following algorithm is used.</span></span>

<span data-ttu-id="d252a-602">Künstliche Steuerungs Punkte werden eingeführt, um das Verhalten der Polynomials in Regionen mit unzureichender Stichprobenentnahme zu steuern.</span><span class="sxs-lookup"><span data-stu-id="d252a-602">Artificial control points are introduced to control the behavior of the polynomials in regions with insufficient sampling.</span></span> <span data-ttu-id="d252a-603">Wenn Sie diese Steuerungs Punkte strategisch mit den entsprechenden Werten platzieren, können Sie die Polynomen in der gewünschten Richtung "abrufen".</span><span class="sxs-lookup"><span data-stu-id="d252a-603">By strategically placing these control points with appropriate values, they serve to "pull" the polynomials in the required direction.</span></span> <span data-ttu-id="d252a-604">In der aktuellen Implementierung werden acht Steuerungs Punkte verwendet, die den Ecken des RGB-Cubes entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d252a-604">In the current implementation, eight control points corresponding to the corners of the RGB cube are used.</span></span> <span data-ttu-id="d252a-605">Wenn die Geräte Werte in Unity normalisiert werden, lauten die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="d252a-605">If the device values are normalized to unity, then these points are:</span></span>

<span data-ttu-id="d252a-606">*R* = 0, *G* = 0, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="d252a-606">*R* = 0, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="d252a-607">*R* = 0, *G* = 0, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="d252a-607">*R* = 0, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="d252a-608">*R* = 0, *G* = 1, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="d252a-608">*R* = 0, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="d252a-609">*R* = 0.</span><span class="sxs-lookup"><span data-stu-id="d252a-609">*R* = 0.</span></span> <span data-ttu-id="d252a-610">*G* = 1, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="d252a-610">*G* = 1, *B* = 1</span></span>

<span data-ttu-id="d252a-611">*R* = 1, *G* = 0, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="d252a-611">*R* = 1, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="d252a-612">*R* = 1, *G* = 0, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="d252a-612">*R* = 1, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="d252a-613">*R* = 1, *G* = 1, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="d252a-613">*R* = 1, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="d252a-614">*R* = 1, *G* = 1, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="d252a-614">*R* = 1, *G* = 1, *B* = 1</span></span>

<span data-ttu-id="d252a-615">Mit Ausnahme von White *R*  = *G*  = *B* = 1, das einem CIELAB-Wert von *L* = 100, *u*  = *v* = 0 zugeordnet ist, wird der folgende Extraktions Algorithmus verwendet, um den entsprechenden CIELAB-Wert zu bestimmen, der zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d252a-615">Except for the white *R* =*G* =*B* = 1, which is associated with a CIELAB value of *L* = 100, *u* =*v* = 0, the following extrapolation algorithm is used to determine the appropriate CIELAB value to be associated with.</span></span> <span data-ttu-id="d252a-616">Im Allgemeinen wird für eine bestimmte (*r*,*g*,*b* ) eine Gewichtung mit jedem der (*r <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) im Stichproben DataSet verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d252a-616">Generally, for a given (*R*,*G*,*B* ), a weight is associated with each of the (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ) in the sampled data set.</span></span> <span data-ttu-id="d252a-617">Es gibt zwei Ziele, die Gewichtung zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="d252a-617">There are two goals to assigning the weight.</span></span> <span data-ttu-id="d252a-618">Zuerst ist die Gewichtung umgekehrt proportional zu der Entfernung zwischen (*r*,*g*,*B* ) und (*r <sub>i</sub>*,*g <sub>i</sub>*,*b <sub>i</sub>* ).</span><span class="sxs-lookup"><span data-stu-id="d252a-618">First, the weight is inversely proportional to the distance between (*R*,*G*,*B* ) and (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ).</span></span> <span data-ttu-id="d252a-619">Zweitens: Sie möchten 0 (null) oder 0 (null) an Punkte verwerfen, die einen anderen Farbton als den angegebenen Punkt aufweisen (*R*,*G*,*B* ).</span><span class="sxs-lookup"><span data-stu-id="d252a-619">Second, you want to discard, or assign weight 0 to, points that have a different hue than the given point (*R*,*G*,*B* ).</span></span> <span data-ttu-id="d252a-620">Um den Farbton zu berücksichtigen, berücksichtigen Sie Punkte, die sich in einem Kegel befinden, dessen Scheitelpunkt bei (0,0) liegt, dessen Achse mit dem Zeilen Beitritt (0, 0, 0) zu (*R*,*G*,*B* ) und einem semivertikalen Winkel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d252a-620">To take the hue into account, consider points that lie within a cone whose vertex is at (0, 0, 0), whose axis coincides with the line joining (0, 0, 0) to (*R*,*G*,*B* ), and whose semi-vertical angle ?</span></span> <span data-ttu-id="d252a-621">erfüllt COS?</span><span class="sxs-lookup"><span data-stu-id="d252a-621">satisfies cos ?</span></span> <span data-ttu-id="d252a-622">= 0,9.</span><span class="sxs-lookup"><span data-stu-id="d252a-622">= 0.9.</span></span> <span data-ttu-id="d252a-623">Eine Abbildung dieses Kegel finden Sie in Abbildung 3.</span><span class="sxs-lookup"><span data-stu-id="d252a-623">See Figure 3 for an illustration of this cone.</span></span>

![Diagramm, das die Form der Umgebung anzeigt.](images/cdmp-lcd-dmp-figure3.png)

<span data-ttu-id="d252a-625">**Abbildung 3** : Filtern der Beispiel Punkte nach Winkel und Entfernung.</span><span class="sxs-lookup"><span data-stu-id="d252a-625">**Figure 3** : Filtering the sample points by angle and distance.</span></span> <span data-ttu-id="d252a-626">Die Form der dargestellten Umgebung dient nur der Veranschaulichung.</span><span class="sxs-lookup"><span data-stu-id="d252a-626">The shape of the neighborhood depicted is for illustration purpose only.</span></span> <span data-ttu-id="d252a-627">Die tatsächliche Form hängt von der verwendeten Entfernung ab. Wenn die 1-Norm verwendet wird, handelt es sich um eine rautenförmige Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d252a-627">The actual shape depends on the distance used; it is a diamond-shaped neighborhood if the 1-norm is used.</span></span>

<span data-ttu-id="d252a-628">Innerhalb dieses Kegel wird eine zweite Filterung durchgeführt, die auf der RGB-Distanz basiert, die die durch</span><span class="sxs-lookup"><span data-stu-id="d252a-628">Within this cone, a second filtering is performed that is based on the RGB distance, which uses the 1-norm, defined by</span></span>

![Zeigt die Formel für das zweite Filtern im Kegel an.](images/cdmp-formula28.png)

<span data-ttu-id="d252a-630">Beim aktuellen Kegel ist die erste Suche nach Punkten, die innerhalb eines Entfernungs von 0,1 von (*R*,*G*,*B* ) liegen.</span><span class="sxs-lookup"><span data-stu-id="d252a-630">With the current cone, the initial search is for points that are within a distance of 0.1 from (*R*,*G*,*B* ).</span></span> <span data-ttu-id="d252a-631">Wenn in diesem RADIUS kein Punkt gefunden wird, wird der Radius um 0,1 erweitert, und die Suche wird neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="d252a-631">If no point is found within this radius, the radius is increased by 0.1, and the search is restarted.</span></span> <span data-ttu-id="d252a-632">Wenn die nächsten Runden Netze keinen Punkt haben, wird der Radius um 0,1 erweitert.</span><span class="sxs-lookup"><span data-stu-id="d252a-632">If the next round nets no point either, the radius is increased by 0.1.</span></span> <span data-ttu-id="d252a-633">Dieser Prozess wird fortgesetzt, bis der RADIUS maxdist/5 überschreitet, wobei maxdist = 3 im Fall von 1-Norm liegt.</span><span class="sxs-lookup"><span data-stu-id="d252a-633">This process continues until the radius exceeds MaxDist/5, where MaxDist = 3, in the case of 1-norm.</span></span> <span data-ttu-id="d252a-634">Wenn kein Punkt gefunden wird, wird der Kegel durch Verringern der cos vergrößert?</span><span class="sxs-lookup"><span data-stu-id="d252a-634">If no point is found, the cone is enlarged by decreasing the cos ?</span></span> <span data-ttu-id="d252a-635">um 0,05, also das Erhöhen des Winkels?</span><span class="sxs-lookup"><span data-stu-id="d252a-635">by 0.05, that is, increasing the angle ?</span></span> <span data-ttu-id="d252a-636">und den gesamten Prozess mit einem zunehmenden RADIUS neu starten.</span><span class="sxs-lookup"><span data-stu-id="d252a-636">and restarting the whole process with an increasing radius.</span></span> <span data-ttu-id="d252a-637">Dieser Prozess wird fortgesetzt, bis ein nicht leerer Satz von Punkten gefunden wird, oder COS?</span><span class="sxs-lookup"><span data-stu-id="d252a-637">This process continues until a non-empty set of points is found, or cos ?</span></span> <span data-ttu-id="d252a-638">erreicht 0, d. h., der Kegel wurde als Ebene geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d252a-638">reaches 0, that is, the cone has opened up to become a plane.</span></span> <span data-ttu-id="d252a-639">An diesem Punkt wird die Suche durch Erhöhen des RADIUS neu gestartet, mit der Ausnahme, dass die Suche so lange fortgesetzt wird, bis der RADIUS maxdist erreicht.</span><span class="sxs-lookup"><span data-stu-id="d252a-639">At this point, the search is restarted by increasing the radius, except that the search continues until the radius reaches MaxDist.</span></span> <span data-ttu-id="d252a-640">Dadurch wird sichergestellt, dass im ungünstigsten Fall ein nicht leerer Satz von Punkten gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="d252a-640">This guarantees that in the worst-case scenario, a non-empty set of points will be found.</span></span> <span data-ttu-id="d252a-641">Der Algorithmus wird im Flussdiagramm in Abbildung 4 zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="d252a-641">The algorithm is summarized in the flow diagram in Figure 4.</span></span>

![Diagramm, das den Ablauf des Algorithmus anzeigt.](images/cdmp-lcd-dmp-figure4.png)

<span data-ttu-id="d252a-643">**Abbildung 4** : Flussdiagramm zum Bestimmen der in der extrapolierungs Gruppe verwendeten Beispiel Punkte für einen Eingabe-RGB-Wert</span><span class="sxs-lookup"><span data-stu-id="d252a-643">**Figure 4** : Flow diagram for determining the set S of sample points used in the extrapolation for an input RGB value</span></span>

<span data-ttu-id="d252a-644">Angenommen, der vorherige Prozess ergibt eine nicht *leere Gruppe von* Punkten (*R <sub>i</sub>*,*G <sub>i</sub>*,*b <sub>i</sub>* ) und entsprechende (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), dann wird für jeden dieser Punkte eine Gewichtungs *w <sub>i</sub>* zugewiesen, angegeben durch</span><span class="sxs-lookup"><span data-stu-id="d252a-644">Assuming that the preceding process yields a non-empty set *S* of points (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) and corresponding (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), then for each such point, a weight *w<sub>i</sub>* is assigned, given by</span></span>

![Zeigt die Formel für eine Gewichtung für jeden Punkt an.](images/cdmp-formula29.png)

<span data-ttu-id="d252a-646">Schließlich wird der extrapolier definiert durch</span><span class="sxs-lookup"><span data-stu-id="d252a-646">Finally, the extrapolant is defined by</span></span>

![Zeigt die Definition für die extrapolier.](images/cdmp-formula30.png)

<span data-ttu-id="d252a-648">Die vorstehenden Gleichungen bilden eine Instanz der "mit umgekehrter Entfernung gewichteten Methoden", die in der Regel als Shepard-Methoden bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-648">The preceding equations constitute an instance of the "inverse-distance weighted methods," commonly called the Shepard methods.</span></span> <span data-ttu-id="d252a-649">Wenn Sie jeden der acht Punkte von EQ (6) über den Algorithmus ausführen, werden acht Steuerungs Punkte abgerufen, jeweils mit den Werten *R*,*G*,*b* und *L*,*a* und *B* , die mit den ursprünglichen Beispiel Daten in den Pool eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-649">By running each of the eight points from eq (6) through the algorithm, eight control points are obtained, each with *R*,*G*,*B* and *L*,*a*,*b* values, which are put into the pool with the original sample data.</span></span>

<span data-ttu-id="d252a-650">Um sicherzustellen, dass das Modell immer gültige Farbwerte und die Systemintegrität und die Stabilität der gesamten farbverarbeitungs Pipeline generiert, müssen Sie ein endgültiges Abschneiden der Ausgabe des Polynoms-Modells durchführen.</span><span class="sxs-lookup"><span data-stu-id="d252a-650">To ensure that the model always produces valid color values and for system integrity and stability down the whole color processing pipeline, you must perform a final clipping to the output of the polynomial model.</span></span> <span data-ttu-id="d252a-651">Der visuelle Bereich von Cie wird von der achrogmatischen Komponente (*Y* oder *L* ) und der chromatischen Komponente (*XY* oder *a' b '* beschrieben, die mit dem XYZ-Raum durch eine projektive Transformation verknüpft ist).</span><span class="sxs-lookup"><span data-stu-id="d252a-651">The CIE visual gamut is described by the achromatic component (*Y* or *L* ) and the chromatic component (*xy* or *a'b'*, which are related to the XYZ space by a projective transformation).</span></span> <span data-ttu-id="d252a-652">In der aktuellen Implementierung wird die Chromatizität der *b ' b '* verwendet, da Sie direkt mit dem CIELUV-Raum verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="d252a-652">In the current implementation, the *a'b'* chromaticity is used because it is directly related to the CIELUV space.</span></span> <span data-ttu-id="d252a-653">Für jeden *CIELAB* -Wert wird " *L* " zuerst auf einen nicht negativen Wert zugeschnitten:</span><span class="sxs-lookup"><span data-stu-id="d252a-653">For any *CIELAB* value, first clip *L* to a non-negative value:</span></span>

![Zeigt das Abschneiden von L auf einen nicht negativen Wert an.](images/cdmp-formula31.png)

<span data-ttu-id="d252a-655">Um das extrapolieren für Glanzlichter zu ermöglichen, wird *L* nicht um 100 abgeschnitten, d. h. die "konventionelle" Obergrenze für *L* im Lab-Bereich.</span><span class="sxs-lookup"><span data-stu-id="d252a-655">To allow extrapolation for specular highlights, *L* is not clipped at 100, the "conventional" upper bound for *L* in Lab space.</span></span>

<span data-ttu-id="d252a-656">Wenn *L* = 0 ist, werden *a* und *b* abgeschnitten, sodass a *= b =* 0 ist.</span><span class="sxs-lookup"><span data-stu-id="d252a-656">Next, if *L* = 0, then *a* and *b* are clipped such that a *= b =* 0.</span></span> <span data-ttu-id="d252a-657">Wenn *L* ?</span><span class="sxs-lookup"><span data-stu-id="d252a-657">If *L* ?</span></span> <span data-ttu-id="d252a-658">0, berechnen</span><span class="sxs-lookup"><span data-stu-id="d252a-658">0, calculate</span></span>

![Zeigt die Formel an, wenn L = 0.](images/cdmp-formula32.png)

<span data-ttu-id="d252a-660">Dabei handelt es sich um die Komponenten eines Vektors im ' *b* '-Diagramm vom weißen Punkt (*u? '*,*v? '* ).</span><span class="sxs-lookup"><span data-stu-id="d252a-660">These are the components of a vector in the *a'b'* diagram from the white point (*u?'*,*v?'*</span></span> <span data-ttu-id="d252a-661">) auf die betreffende Farbe.</span><span class="sxs-lookup"><span data-stu-id="d252a-661">) to the color in question.</span></span> <span data-ttu-id="d252a-662">Definieren Sie den Speicherort des Cie-Spektrums als die zusammen gezierte Hülle aller Punkte (*a '*,*b '* ), die durch die Wellenlinie parametrisiert werden?:</span><span class="sxs-lookup"><span data-stu-id="d252a-662">Define the CIE spectral locus as the convex hull of all the points (*a'*,*b'* ), parameterized by the wavelength ?:</span></span>

![Zeigt die Formel für die-Wellen Wellen an.](images/cdmp-formula33.png)

<span data-ttu-id="d252a-664">dabei ![ zeigt die Funktionen für den Cie-Farbabgleich an.](images/cdmp-formula34.png)</span><span class="sxs-lookup"><span data-stu-id="d252a-664">where ![Shows the functions for CIE color-matching.](images/cdmp-formula34.png)</span></span> <span data-ttu-id="d252a-665">die Funktionen der Cie-Farb Übereinstimmung für den 2-Grad-Beobachter.</span><span class="sxs-lookup"><span data-stu-id="d252a-665">are the CIE color-matching functions for the 2-degree observer.</span></span> <span data-ttu-id="d252a-666">Wenn der Vektor außerhalb des Cie-Ursprung liegt, wird die Farbe auf den Punkt auf dem Cie-Lokus zugeschnitten, bei dem es sich um die Schnittmenge des Lokus und die durch den Vektor definierte Linie handelt.</span><span class="sxs-lookup"><span data-stu-id="d252a-666">If the vector lies outside the CIE locus, the color is clipped to the point on the CIE locus that is the intersection of the locus and the line defined by the vector.</span></span> <span data-ttu-id="d252a-667">Weitere Informationen in Abbildung 5.</span><span class="sxs-lookup"><span data-stu-id="d252a-667">See Figure 5.</span></span> <span data-ttu-id="d252a-668">Wenn Clipping aufgetreten ist, wird der *a* -Wert und der *b* -Wert durch erstes subtrahieren *eines?* -Werts rekonstruiert.</span><span class="sxs-lookup"><span data-stu-id="d252a-668">If clipping has occurred, the *a* and *b* value is reconstructed by first subtracting *a?'*</span></span> <span data-ttu-id="d252a-669">und *b? "*</span><span class="sxs-lookup"><span data-stu-id="d252a-669">and *b?'*</span></span> <span data-ttu-id="d252a-670">aus dem abgeschnitten *a '* und *b '* und dann mit 13 *L* multipliziert.</span><span class="sxs-lookup"><span data-stu-id="d252a-670">from the clipped *a'* and *b'*, and then multiplying by 13 *L*.</span></span>

![Diagramm, das das Diagramm für den clippingalgorithmus anzeigt.](images/cdmp-lcd-dmp-figure5.png)

<span data-ttu-id="d252a-672">**Abbildung 5** : Clipping-Algorithmus für Lab-Werte, die sich außerhalb des Sichtbarkeit von Cie befinden</span><span class="sxs-lookup"><span data-stu-id="d252a-672">**Figure 5** : Clipping algorithm for Lab values that are outside the CIE visual gamut</span></span>

<span data-ttu-id="d252a-673">In der aktuellen Implementierung wird der Cie-spektrallokus in der Ebene der *b ' b '* durch eine schrittweise lineare Kurve mit 35 Segmenten dargestellt (entsprechend einer Wellenlinie zwischen 360 nm und 700 nm).</span><span class="sxs-lookup"><span data-stu-id="d252a-673">In the current implementation, the CIE spectral locus in the *a'b'* plane is represented by a piecewise linear curve with 35 segments (corresponding to a wavelength from 360 nm to 700 nm inclusive).</span></span> <span data-ttu-id="d252a-674">Wenn Sie die Liniensegmente so sortieren, dass ihre untergeordneten Winkel am weißen Punkt aufsteigend sind, was absteigender Wellenlinien entspricht, kann das Liniensegment, das sich mit dem durch den obigen Vektor geformten Strahl schneidet, durch eine einfache binäre Suche gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-674">By ordering the line segments so that their subtended angles at the white point are ascending, which is equivalent to descending wavelengths, the line segment that intersects with the ray formed by the above vector can be found by a simple binary search.</span></span>

### <a name="rgb-printer-device-model-baseline"></a><span data-ttu-id="d252a-675">Basislinie des RGB-Drucker Geräte Modells</span><span class="sxs-lookup"><span data-stu-id="d252a-675">RGB Printer Device Model Baseline</span></span>

<span data-ttu-id="d252a-676">Eine Geräte Charakterisierung eines RGB-Druckers besteht aus der Erstellung eines empirisch basierenden Modells des Geräts, das die geräteunabhängige CIELUV-Farbe für einen beliebigen RGB-Wert vorhersagt.</span><span class="sxs-lookup"><span data-stu-id="d252a-676">A device characterization of a RGB printer consists of constructing an empirical model of the device that predicts the device-independent CIELUV color for any given RGB value</span></span>

<span data-ttu-id="d252a-677">Es gibt zwei Möglichkeiten, das empirische Modell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d252a-677">There are two ways to construct the empirical model.</span></span> <span data-ttu-id="d252a-678">Eine Möglichkeit besteht darin, die Gerätedaten für einen RGB-Drucker zu verwenden, und das andere die Verwendung analytischer Parameterdaten.</span><span class="sxs-lookup"><span data-stu-id="d252a-678">One way is to use the device data for a RGB printer, and the other is to use analytical parameter data.</span></span> <span data-ttu-id="d252a-679">Im ersten wird die von einem Benutzer für ein RGB-Druckergerät bereitgestellte Messungs Daten verwendet, um eine 3D-Nachschlage Tabelle (Data-D Suche Table, LUT) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d252a-679">In the first one, measurement data provided by a user for a RGB printer device is used to construct 3-D lookup table (LUT).</span></span> <span data-ttu-id="d252a-680">Die Mess Daten bestehen aus XYZ-Werten für bei gleichmäßigen Stichproben von RGB-Patches.</span><span class="sxs-lookup"><span data-stu-id="d252a-680">The measurement data consists of XYZ values for uniformly sampled RGB patches.</span></span> <span data-ttu-id="d252a-681">Typische Stichprobengrößen sind für jede Komponente 9 oder 17.</span><span class="sxs-lookup"><span data-stu-id="d252a-681">Typical sampling sizes are 9 or 17 for each component.</span></span> <span data-ttu-id="d252a-682">Jeder Patch wird mit einem Farbwert oder einem Spektrophotometer im CIEXYZ-Raum gemessen.</span><span class="sxs-lookup"><span data-stu-id="d252a-682">Each patch is measured with a colorimeter or spectrophotometer in CIEXYZ space.</span></span> <span data-ttu-id="d252a-683">Der XYZ-Wert für einen Patch wird dann in einen CIELUV-Wert konvertiert, der einen 3D-LUT bildet.</span><span class="sxs-lookup"><span data-stu-id="d252a-683">The XYZ value for a patch is then converted into CIELUV value, forming a 3-D LUT.</span></span> <span data-ttu-id="d252a-684">Im Gerätemodell wird die Methode "tetrahedral Interpolationsmethode" von Sakamoto auf den 3D-Kanal angewendet, um die CIELUV-Daten für eine bestimmte RGB-Daten vorherzusagen.</span><span class="sxs-lookup"><span data-stu-id="d252a-684">In the device model, the Sakamoto's tetrahedral interpolation method is applied to the 3-D LUT in order to predict the CIELUV data for a given RGB data.</span></span> <span data-ttu-id="d252a-685">(Erteilen Sie die US-Patent 4275413 (Sakamoto et al.), US-Patent 4511989 (Sakamoto), Kang \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="d252a-685">(Confer US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="d252a-686">Die zwei erwähnten Patente sind abgelaufen.)</span><span class="sxs-lookup"><span data-stu-id="d252a-686">The two patents mentioned have expired.).</span></span> <span data-ttu-id="d252a-687">Bei den in der zweiten Methode übergebenen analytischen Parameterdaten handelt es sich einfach um einen zuvor erstellten LUT.</span><span class="sxs-lookup"><span data-stu-id="d252a-687">The analytical parameter data passed in the second method is simply a LUT that was built previously.</span></span> <span data-ttu-id="d252a-688">In der Regel wurde dieser LUT mithilfe der ersten Methode erstellt, obwohl er möglicherweise Hand erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d252a-688">Typically, that LUT was built using the first method, although it could be hand-built.</span></span>

<span data-ttu-id="d252a-689">In der aktuellen Farbverwaltung wird die Quell Zuordnung als die Zuordnung definiert, die von RGB-Leerraum zu einem geräteunabhängigen CIEXYZ-Farbraum übergeht.</span><span class="sxs-lookup"><span data-stu-id="d252a-689">In the current color management, the source map is defined as the map that goes from RGB space to a device-independent CIEXYZ color space.</span></span> <span data-ttu-id="d252a-690">Die Ziel Zuordnung wird als die Zuordnung definiert, die vom geräteunabhängigen CIEXYZ-Farbraum zu RGB-Speicherplatz reicht.</span><span class="sxs-lookup"><span data-stu-id="d252a-690">The destination map is defined as the map that goes from the device-independent CIEXYZ color space to RGB space.</span></span> <span data-ttu-id="d252a-691">Dies ist die Umkehrung der Quell Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="d252a-691">It is the inverse of the source map.</span></span>

<span data-ttu-id="d252a-692">Das empirische Modell wird direkt in der Quell Zuordnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-692">The empirical model is directly used in the source map.</span></span> <span data-ttu-id="d252a-693">Zuerst werden die angegebenen RGB-Daten einer CIELUV-Daten zugeordnet, die in XYZ-Daten konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-693">It first maps a given RGB data into a CIELUV data, which is converted into XYZ data.</span></span> <span data-ttu-id="d252a-694">In der Ziel Zuordnung werden geräteunabhängige CIEXYZ-Daten zuerst in CIELUV-Daten konvertiert.</span><span class="sxs-lookup"><span data-stu-id="d252a-694">In the destination map, device-independent CIEXYZ data is first converted into CIELUV data.</span></span> <span data-ttu-id="d252a-695">Anschließend werden das empirische Modell und die klassische Newton-Raphson-Methode verwendet, um die besten RGB-Daten für die CIELUV-Daten vorherzusagen.</span><span class="sxs-lookup"><span data-stu-id="d252a-695">Then, the empirical model and the classical Newton-Raphson method are used to predict the best RGB data for the CIELUV data.</span></span> <span data-ttu-id="d252a-696">Die Details zur Konvertierung von CIELUV in RGB-Daten lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d252a-696">The details about conversion from CieLUV to RGB data are as follows:</span></span>

<span data-ttu-id="d252a-697">Nachdem Sie einen 3D-Kanal von RGB zu CIELUV erstellt haben, wird die Zuordnung zwischen RGB und Luv mithilfe der tetrahedral-interpolung auf RGB erstellt.</span><span class="sxs-lookup"><span data-stu-id="d252a-697">After generating a 3-D LUT from RGB to CieLUV, the map from RGB to LUV is built using tetrahedral interpolation on RGB.</span></span> <span data-ttu-id="d252a-698">Diese Zuordnung wird durch die folgenden Gleichungen bezeichnet:</span><span class="sxs-lookup"><span data-stu-id="d252a-698">This map is denoted by the following equations:</span></span>

![Zeigt die Gleichungen für die Karte von R G B bis L U V an.](images/cdmp-image125.png)

<span data-ttu-id="d252a-700">Die Inversion der Zuordnung besteht aus der Lösung für beliebige Farben.</span><span class="sxs-lookup"><span data-stu-id="d252a-700">Inversion of the map consists of solving, for any color</span></span> ![Zeigt L U V an.](images/cdmp-image127.png) <span data-ttu-id="d252a-702">, das folgende System nichtlinearer Gleichungen:</span><span class="sxs-lookup"><span data-stu-id="d252a-702">, the following system of nonlinear equations:</span></span>

![Zeigt die nichtlinearen Gleichungen für das lolving beliebiger Farbe L U V an.](images/cdmp-image129.png)

<span data-ttu-id="d252a-704">Eine nichtlineare Gleichung, die auf der klassischen Newton-Raphson-Methode basiert, wird im neuen allgemeinen Tabellen Ausdruck (CTE) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-704">A nonlinear equation that is based on the classical Newton-Raphson method is used in the new CTE.</span></span> <span data-ttu-id="d252a-705">Ein ursprünglicher Schätzwert bzw. *a* -Wert, der <sub>vor</sub> (R 0, G 0, B 0) liegt, wird durch Durchsuchen einer "Seed Matrix" abgerufen, die aus einem einheitlichen 8x8x8-Raster mit vorab berechneten (RGB-, Luv-) Paaren besteht.</span><span class="sxs-lookup"><span data-stu-id="d252a-705">An initial guess, or *a priori* see, s <sub>prior</sub> -(R 0, G 0, B 0 ) is obtained by searching through a "seed matrix" consisting of a uniform 8x8x8 grid of pre-computed (RGB,Luv) pairs.</span></span> <span data-ttu-id="d252a-706">Die entsprechende RGB-Luv, die der L u v am nächsten ist, \* \* \* wird ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d252a-706">The RGB corresponding Luv that is closest to the L\*u\*v\* is chosen.</span></span> <span data-ttu-id="d252a-707">Jeder Punkt in der Seed-Matrix entspricht dem Mittelpunkt einer Zelle, sodass die Iterationen nicht mit einem Punkt an der Begrenzungs Seite des RGB-Cubes beginnen.</span><span class="sxs-lookup"><span data-stu-id="d252a-707">Each point in the seed matrix corresponds to the center of a cell so that the iterations don't start with a point on the boundary face of the RGB cube.</span></span> <span data-ttu-id="d252a-708">Mit anderen Worten: der RGB der Kerne wird durch Folgendes definiert: Schritt = 1/8 s <sub>IJK</sub> = (Schritt/2 + (i-1) Schritt, Schritt/2 + (j-1) Schritt, Schritt/2 + (k-1) Schritt) mit i, j, k = 1... 8 im *i* . Schritt von Newton-Raphson zeigt die nächste Schätzung ![ die Variablen für die nächste Schätzung an.](images/cdmp-image133.png)</span><span class="sxs-lookup"><span data-stu-id="d252a-708">In other words, the RGB of the seeds is defined by: STEP = 1/8 s <sub>ijk</sub> = (STEP/2 + (i-1) STEP, STEP/2+(j-1)STEP, STEP/2+(k-1)STEP) with i,j,k = 1...8 At the *i* th step of Newton-Raphson, the next estimate ![Shows the variables for the next estimate.](images/cdmp-image133.png)</span></span> <span data-ttu-id="d252a-709">wird von der Formel abgerufen:</span><span class="sxs-lookup"><span data-stu-id="d252a-709">is obtained by the formula:</span></span>

![Zeigt die Formel für die Schätzung an.](images/cdmp-image135.png)

<span data-ttu-id="d252a-711">Die Iteration wird beendet, wenn der Fehler (Entfernung im CIELUV-Bereich) kleiner ist als eine voreingebene Toleranzstufe (0,1 im CTE) oder wenn die Anzahl der Iterationen die maximal zulässige Anzahl von Iterationen überschreitet (10 in der CTE).</span><span class="sxs-lookup"><span data-stu-id="d252a-711">Iteration stops when the error (distance in the CIELUV space) is less than a pre-set tolerance level (0.1 in the CTE), or when the number of iterations has exceeded the maximum allowed number of iterations (10 in the CTE).</span></span> <span data-ttu-id="d252a-712">Die Werte für die Toleranz und die Anzahl der Iterationen wurden empirisch als wirksam festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d252a-712">The values for the tolerance and the number of iterations were empirically determined to be effective.</span></span> <span data-ttu-id="d252a-713">In zukünftigen Versionen kann der Toleranzwert geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-713">In future versions, the tolerance value may be changed.</span></span>

<span data-ttu-id="d252a-714">Die Jacobian-Matrix wird mithilfe der Forward-Differenz berechnet, außer an einem Begrenzungs Punkt (mindestens eine R, G, B ist 1), wobei der abwärts Unterschied stattdessen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d252a-714">The Jacobian matrix is calculated using forward difference, except at a boundary point (one or more of the R, G, B is 1) where backward difference is used instead.</span></span> <span data-ttu-id="d252a-715">Anstatt die Umkehrung der Jacobian-Matrix zu berechnen, wird das lineare System mithilfe der Gauss-Jordan Beseitigung mit vollständigem pivotieren direkt gelöst.</span><span class="sxs-lookup"><span data-stu-id="d252a-715">Instead of calculating the inverse of the Jacobian matrix, the linear system is solved directly using Gauss-Jordan elimination with full pivoting.</span></span>

<span data-ttu-id="d252a-716">Am Ende der Iterationen wird die Konvergenz möglicherweise noch nicht erreicht, da Newton-Raphson ein "lokaler" Algorithmus ist, das heißt, dass Sie nur dann gut funktioniert, wenn Sie mit einer anfänglichen Schätzung beginnen, die in der Nähe der echten Lösung liegt.</span><span class="sxs-lookup"><span data-stu-id="d252a-716">At the end of the iterations, convergence still might not be achieved because Newton-Raphson is a "local" algorithm, that is, it only works well if you start with an initial guess that is close to the true solution.</span></span> <span data-ttu-id="d252a-717">Wenn am Ende der Newton-Raphson Iterationen die Konvergenz innerhalb der vordefinierten Fehlertoleranz nicht erreicht wurde, werden die Iterationen mit einem neuen Satz von Kernen neu gestartet, die wie folgt definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-717">If, at the end of the Newton-Raphson iterations, convergence within the pre-defined error tolerance has not been achieved, the iterations are restarted with a new set of seeds, defined as follows.</span></span>

<span data-ttu-id="d252a-718">Die bisher beste Lösung ist beispielsweise (r, g, b).</span><span class="sxs-lookup"><span data-stu-id="d252a-718">For example, the best solution obtained so far is (r, g, b).</span></span> <span data-ttu-id="d252a-719">Aus dieser Lösung werden n a-posteriori-Kerne abgeleitet, wobei n = 4 ist.</span><span class="sxs-lookup"><span data-stu-id="d252a-719">From this solution, N a posteriori seeds are derived, where N = 4.</span></span> <span data-ttu-id="d252a-720">Die Projekt Mappe wird intuitiv in eine Schrittgröße verschoben, die von N abhängig ist. Siehe Abbildung 6.</span><span class="sxs-lookup"><span data-stu-id="d252a-720">Intuitively, the solution is moved "toward the center" in a step size that depends on N. See Figure 6.</span></span>

![Diagramm, das die Richtung der Projekt Mappe enthält.](images/cdmp-image136.png)

<span data-ttu-id="d252a-722">**Abbildung 6** : die Zuordnungs Richtung der Lösung hängt davon ab, in welchem Octant Sie sich befindet.</span><span class="sxs-lookup"><span data-stu-id="d252a-722">**Figure 6** : Perturbation direction of the solution depends on which octant it is in.</span></span>

<span data-ttu-id="d252a-723">Anders ausgedrückt: wenn r &gt; 0,5, wird der Wert im r-Kanal verringert; andernfalls wird der Wert angehoben.</span><span class="sxs-lookup"><span data-stu-id="d252a-723">In other words, if r &gt; 0.5, the value on the R channel is decreased, otherwise the value is increased.</span></span> <span data-ttu-id="d252a-724">Es gibt eine ähnliche Logik für die Kanäle "G" und "B".</span><span class="sxs-lookup"><span data-stu-id="d252a-724">There is similar logic for the G and B channels.</span></span> <span data-ttu-id="d252a-725">Die genauen Definitionen lauten:</span><span class="sxs-lookup"><span data-stu-id="d252a-725">The precise definitions are:</span></span>

<span data-ttu-id="d252a-726">Perturbation = 0.5/(N + 1)</span><span class="sxs-lookup"><span data-stu-id="d252a-726">PERTURBATION = 0.5/(N+1)</span></span>

<span data-ttu-id="d252a-727">Dir (r) =-1, wenn r &gt; 0,5; + 1 andernfalls.</span><span class="sxs-lookup"><span data-stu-id="d252a-727">Dir(r) = -1 if r &gt; 0.5; +1 otherwise.</span></span> <span data-ttu-id="d252a-728">Gleiches gilt für dir (g) und dir (b).</span><span class="sxs-lookup"><span data-stu-id="d252a-728">Similarly for Dir(g) and Dir(b)</span></span>

<span data-ttu-id="d252a-729">Der Jth a posteriori Seed, s????, ist (r + dir (r) \* j \* Perturbation, g + dir (g) \* j \* Perturbation, b + dir (b) \* j \* Perturbation)</span><span class="sxs-lookup"><span data-stu-id="d252a-729">The jth a posteriori seed, s ????, is (r + Dir(r) \*j \* PERTURBATION, g + Dir(g) \* j \* PERTURBATION, b + Dir(b) \* j \* PERTURBATION)</span></span>

<span data-ttu-id="d252a-730">Testen Sie die ersten s????</span><span class="sxs-lookup"><span data-stu-id="d252a-730">Try the first s ????</span></span> <span data-ttu-id="d252a-731">Wenn eine neue Projekt Mappe in der Fehlertoleranz angezeigt wird, können Sie den Vorgang abbrechen.</span><span class="sxs-lookup"><span data-stu-id="d252a-731">and if it gives a new solution within error tolerance, you can stop.</span></span> <span data-ttu-id="d252a-732">Andernfalls können Sie die zweiten s????</span><span class="sxs-lookup"><span data-stu-id="d252a-732">Otherwise, try the second s ????</span></span> <span data-ttu-id="d252a-733">usw., bis die n-ten????.</span><span class="sxs-lookup"><span data-stu-id="d252a-733">and so on until the Nth s ????.</span></span>

<span data-ttu-id="d252a-734">Die schematiken des gesamten Algorithmus sind in Abbildung 7 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d252a-734">The schematics of the whole algorithm is shown in Figure 7.</span></span>

![Diagramm, das den Ablauf für das Umkehren des Geräte Modells anzeigt.](images/cdmp-image138.png)

<span data-ttu-id="d252a-736">**Abbildung 7** : schematiken zum Umkehren des Geräte Modells</span><span class="sxs-lookup"><span data-stu-id="d252a-736">**Figure 7** : Schematics of inverting the device model</span></span>

### <a name="rgb-virtual-device-model-baseline"></a><span data-ttu-id="d252a-737">Grundlegende Konfiguration des virtuellen Geräte Modells</span><span class="sxs-lookup"><span data-stu-id="d252a-737">RGB Virtual Device Model Baseline</span></span>

<span data-ttu-id="d252a-738">Bei diesem Gerätemodell (DM) handelt es sich um einen einfachen Matrix-/Ton-Reproduktions Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="d252a-738">This device model(DM) is a simple matrix/tone reproduction algorithm.</span></span> <span data-ttu-id="d252a-739">Die Matrix wird aus dem weißen Punkt und den primären Replikaten mithilfe von standardmäßigen Color Science-Algorithmen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d252a-739">The matrix is derived from the white point and primaries using standard color science algorithms.</span></span> <span data-ttu-id="d252a-740">Die audioreproduktions Kurve wird von den Messparametern gemäß den ICC-Beschreibungen von Cursor Type und ParameterType abgeleitet (oder bei Bedarf umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="d252a-740">The tone reproduction curve is derived from the measurement parameters according to the ICC descriptions of CurveType and ParametricType (or inverted as required).</span></span> <span data-ttu-id="d252a-741">Details zu den internen Algorithmen werden nach der zusätzlichen Validierung von Problemen mit hohem dynamischen Bereich bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d252a-741">Details of the internal algorithms will be provided after additional validation of high dynamic range issues.</span></span>

<span data-ttu-id="d252a-742">Das virtuelle RGB-Gerätemodell ist eine idealisierte Matrix-/Ton-Reproduktions Kurve (RGB), ähnlich wie bei einem Matrix basierten Entwurf mit drei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="d252a-742">The RGB virtual device model is an idealized matrix/tone reproduction curve RGB similar to the ICC three-component matrix-based profile design.</span></span> <span data-ttu-id="d252a-743">Die "Virtual Measurement"-Parameter der DM enthalten einen weißen Punkt Wert (absolute CIEXYZ), RGB-Primärwerte (absolute CIEXYZ) und eine Ton-Reproduktions Kurve, die auf dem hashparameterype und dem Cursor Type in der XML-Formatierung basiert, die mit den DMP-Schemas konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="d252a-743">The "virtual measurement" parameters of the DM include a white point value (absolute CIEXYZ), RGB primary values (absolute CIEXYZ), and a tone reproduction curve that is based on the ICC ParametricCurveType and CurveType in XML formatting consistent with the DMP schemas.</span></span>

<span data-ttu-id="d252a-744">In der folgenden Tabelle sind die-Funktionstyp Codierung für den Parameter "-Parametertyp" und die entsprechende Unterstützung in "irigbvirtualdevicemodelbase" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d252a-744">ICC parametricCurveType function type encoding and corresponding support in IRGBVirtualDeviceModelBase are shown in the following table.</span></span>



| <span data-ttu-id="d252a-745">Funktionstyp</span><span class="sxs-lookup"><span data-stu-id="d252a-745">Function type</span></span>                                         | <span data-ttu-id="d252a-746">Parameter</span><span class="sxs-lookup"><span data-stu-id="d252a-746">Parameters</span></span>                          | <span data-ttu-id="d252a-747">type</span><span class="sxs-lookup"><span data-stu-id="d252a-747">Type</span></span>                                     | <span data-ttu-id="d252a-748">Hinweis</span><span class="sxs-lookup"><span data-stu-id="d252a-748">Note</span></span>                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Zeigt die Funktion "gammatype" an.](images/cdmp-image154.png)<br/> | <span data-ttu-id="d252a-750">g</span><span class="sxs-lookup"><span data-stu-id="d252a-750">g</span></span><br/>              | <span data-ttu-id="d252a-751">Gammatype</span><span class="sxs-lookup"><span data-stu-id="d252a-751">GammaType</span></span><br/>                 | <span data-ttu-id="d252a-752">Allgemeine Implementierung</span><span class="sxs-lookup"><span data-stu-id="d252a-752">Common implementation</span></span><br/>           |
| ![Zeigt die Funktion "gammaoffsetgaintype" an.](images/cdmp-image156.png)<br/> | <span data-ttu-id="d252a-754">GA b</span><span class="sxs-lookup"><span data-stu-id="d252a-754">ga b</span></span><br/>           | <span data-ttu-id="d252a-755">Gammaoffsetgaintype</span><span class="sxs-lookup"><span data-stu-id="d252a-755">GammaOffsetGainType</span></span><br/>       | <span data-ttu-id="d252a-756">Cie 122-1966</span><span class="sxs-lookup"><span data-stu-id="d252a-756">CIE 122-1966</span></span><br/>                    |
| ![Zeigt die Funktion ' gammaoffsetgainoffsettype ' an.](images/cdmp-image158.png)<br/> | <span data-ttu-id="d252a-758">GA b c</span><span class="sxs-lookup"><span data-stu-id="d252a-758">ga b c</span></span><br/>         | <span data-ttu-id="d252a-759">Gammaoffsetgainoffsettype</span><span class="sxs-lookup"><span data-stu-id="d252a-759">GammaOffsetGainOffsetType</span></span><br/> | <span data-ttu-id="d252a-760">IEC 61966-3</span><span class="sxs-lookup"><span data-stu-id="d252a-760">IEC 61966-3</span></span><br/>                     |
| ![Zeigt die Funktion "gammaoffsetgaingaintype" an.](images/cdmp-image160.png)<br/> | <span data-ttu-id="d252a-762">GA b c d</span><span class="sxs-lookup"><span data-stu-id="d252a-762">ga b c d</span></span><br/>       | <span data-ttu-id="d252a-763">Gammaoffsetgaingaintype</span><span class="sxs-lookup"><span data-stu-id="d252a-763">GammaOffsetGainGainType</span></span><br/>   | <span data-ttu-id="d252a-764">IEC 61966-2.1</span><span class="sxs-lookup"><span data-stu-id="d252a-764">IEC 61966-2.1</span></span><br/> <span data-ttu-id="d252a-765">sRGB</span><span class="sxs-lookup"><span data-stu-id="d252a-765">(sRGB)</span></span><br/> |
| ![Zeigt eine Funktion für die Parameter "g a b c d e f" an.](images/cdmp-image162.png)<br/> | <span data-ttu-id="d252a-767">GA b c d e f</span><span class="sxs-lookup"><span data-stu-id="d252a-767">ga b c d e f</span></span><br/>   | <span data-ttu-id="d252a-768">–</span><span class="sxs-lookup"><span data-stu-id="d252a-768">N/A</span></span><br/>                       | <span data-ttu-id="d252a-769">In WCS nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d252a-769">Not supported in WCS</span></span><br/>            |



 

<span data-ttu-id="d252a-770">Die audiokurve für virtuelle RGB-Geräte wird in deviceumcolormetric zwischen den Eingabedaten, pdebug-Elementen und der Matrix Multiplikation angewendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-770">The tone curve for RGB virtual devices is applied in DeviceToColorimetric between the input data, pDeviceColors, and the matrix multiply.</span></span> <span data-ttu-id="d252a-771">Für "colormetricydevice" muss eine Methode zum Umkehren der Tonkurve verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-771">For ColorimetricToDevice, a method must be used to invert the tone curve.</span></span> <span data-ttu-id="d252a-772">In der baselineimplementierung erfolgt dies durch direkte Interpolationen in derselben für deviceumcolormetric verwendeten Tonkurve.</span><span class="sxs-lookup"><span data-stu-id="d252a-772">In the baseline implementation, this is done by direct interpolation in the same tone curve used for DeviceToColorimetric.</span></span>

<span data-ttu-id="d252a-773">Die Kurven sollten in den Profilen als Paare von Zahlen in float-Raum angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-773">The curves should be specified in the profiles as pairs of numbers in float space.</span></span> <span data-ttu-id="d252a-774">Die erste Zahl stellt Werte in PDE vicecolors dar.</span><span class="sxs-lookup"><span data-stu-id="d252a-774">The first number represents values in pDeviceColors.</span></span> <span data-ttu-id="d252a-775">Die zweite Zahl stellt die Ausgabe der Tonkurve dar.</span><span class="sxs-lookup"><span data-stu-id="d252a-775">The second number represents the output of the tone curve.</span></span> <span data-ttu-id="d252a-776">Alle Werte in der Tonkurve müssen zwischen mincolorantused und maxcolorantused liegen.</span><span class="sxs-lookup"><span data-stu-id="d252a-776">All values in the tone curve must be between minColorantUsed and maxColorantUsed.</span></span> <span data-ttu-id="d252a-777">Die Tone-Kurven müssen mindestens zwei Einträge enthalten: eine für mincolorantused und eine für maxcolorantused.</span><span class="sxs-lookup"><span data-stu-id="d252a-777">Tone curves must contain at least two entries: one for minColorantUsed and one for maxColorantUsed.</span></span> <span data-ttu-id="d252a-778">Die maximale Anzahl von Einträgen in der tonecurve beträgt 2048.</span><span class="sxs-lookup"><span data-stu-id="d252a-778">The maximum number of entries in the ToneCurve is 2048.</span></span> <span data-ttu-id="d252a-779">Im Allgemeinen können Sie mit der größeren Anzahl von Einträgen in der Tabelle die Krümmung genauer modellieren.</span><span class="sxs-lookup"><span data-stu-id="d252a-779">In general, the more entries in the table, the more accurately you can model curvature.</span></span> <span data-ttu-id="d252a-780">Zwischen den Einträgen wird eine schrittweise lineare Interpolationen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d252a-780">A piecewise linear interpolation is performed between the entries.</span></span>

<span data-ttu-id="d252a-781">Sie können alternative Interpolations Methoden in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="d252a-781">You might consider alternative interpolation methods.</span></span> <span data-ttu-id="d252a-782">Wenn Sie etwas über das zugrunde liegende Verhalten des Geräts wissen, können Sie mit einer höheren Bestell Kurve weniger Stichproben und ein genaueres Modell verwenden.</span><span class="sxs-lookup"><span data-stu-id="d252a-782">If you know something about the underlying behavior of the device, you can use fewer samples and model more accurately with a higher order curve.</span></span> <span data-ttu-id="d252a-783">Wenn Sie jedoch den falschen Kurstyp verwenden, sind Sie sehr ungenau.</span><span class="sxs-lookup"><span data-stu-id="d252a-783">But if you use the wrong curve type, you will be very inaccurate.</span></span> <span data-ttu-id="d252a-784">Ohne weitere Informationen können Sie den Kurven Typ nicht erraten.</span><span class="sxs-lookup"><span data-stu-id="d252a-784">Without more information, you cannot guess the curve type.</span></span> <span data-ttu-id="d252a-785">Verwenden Sie daher lineare Interpolationen, und stellen Sie viele Datenpunkte bereit.</span><span class="sxs-lookup"><span data-stu-id="d252a-785">So, use linear interpolation and provide many data points.</span></span>

### <a name="cmyk-printer-device-model-baseline"></a><span data-ttu-id="d252a-786">Baseline des CMYK-Drucker Geräte Modells</span><span class="sxs-lookup"><span data-stu-id="d252a-786">CMYK Printer Device Model Baseline</span></span>

<span data-ttu-id="d252a-787">Eine Geräte Charakterisierung eines CMYK-Druckers besteht aus der Konstruktion eines empirisch verwendeten Modells des Geräts, das die gedruckte Farbe für einen beliebigen CMYK-Wert vorhersagt.</span><span class="sxs-lookup"><span data-stu-id="d252a-787">A device characterization of a CMYK printer consists of constructing an empirical model of the device that predicts the printed color for any given CMYK value.</span></span> <span data-ttu-id="d252a-788">Die-Charakterisierung umfasst auch die Inversion dieses Modells, sodass ein Rezept des CMYK-Werts für eine angegebene zu druckende Farbe angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d252a-788">The characterization also includes the inversion of this model so that a prescription of the CMYK value to us for a given color to be printed can be given.</span></span> <span data-ttu-id="d252a-789">Dies wird in der Regel in Bezug auf CIEXYZ oder CIELAB-Wert definiert.</span><span class="sxs-lookup"><span data-stu-id="d252a-789">This is typically defined in terms of CIEXYZ or CIELAB value.</span></span>

<span data-ttu-id="d252a-790">In der Regel wird ein IT-8,7/3-Ziel mit CMYK-Patches verwendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-790">Typically, an IT8.7/3 target containing CMYK patches is used.</span></span> <span data-ttu-id="d252a-791">Die Patches bestehen aus der Stichprobenentnahme des CMYK-Speicherplatzes in einer klar definierten Weise, sodass ein rechteckiges Raster (mit nicht einheitlichem Abstand in C, M, Y und K) gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="d252a-791">The patches consist of sampling of the CMYK space in a well-defined manner so that a rectangular grid (with non-uniform spacing in C, M, Y and K) is formed.</span></span> <span data-ttu-id="d252a-792">Jeder Patch wird dann mit einem farbigen oder einem spektrophoto Meter gemessen.</span><span class="sxs-lookup"><span data-stu-id="d252a-792">Each patch is then measured with a colorimeter or spectrophotometer.</span></span> <span data-ttu-id="d252a-793">Die Messungen in CIEXYZ-Werten bilden dann eine Suche Table (LUT), aus der ein empirisches Modell des Druckers mit der Interpolationsmethode von Sakamoto erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d252a-793">The measurements in CIEXYZ values then form a lookup table (LUT), from which an empirical model of the printer is built using Sakamoto's interpolation method.</span></span> <span data-ttu-id="d252a-794">US-Patent 4275413 (Sakamoto et al.), US-Patent 4511989 (Sakamoto), Kang \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="d252a-794">US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="d252a-795">Die zwei erwähnten Patente sind abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="d252a-795">The two patents mentioned have expired.</span></span>

<span data-ttu-id="d252a-796">Bestimmte Anforderungen an die CMYK-maßproben, die erforderlich sind, damit ein Gerätemodell Profil vom CMYK-druckerbaseline-Gerätemodell als gültig akzeptiert wird, lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="d252a-796">Specific requirements for the CMYK measurement samples necessary for a device model profile to be accepted as valid by the CMYK printer baseline device model are as follows.</span></span> <span data-ttu-id="d252a-797">(Die Stichproben Menge wird in den meisten Fällen als Satz von CMY-Beispielcubes beschrieben, die jeweils mit einer bestimmten K-Ebene verknüpft sind.)</span><span class="sxs-lookup"><span data-stu-id="d252a-797">(The sample set is most clearly described as a set of CMY sample cubes, each associated with a specific K level.)</span></span>

-   <span data-ttu-id="d252a-798">Es müssen mindestens gültige CMY-Cubes für die Ebenen K = 0 und k = 100 bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-798">At minimum, valid CMY cubes must be provided for the K = 0 and K = 100 levels.</span></span>
-   <span data-ttu-id="d252a-799">Zwischen K-Ebenen dürfen nicht gleichmäßig verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-799">Intermediate K levels may be non-uniformly spaced.</span></span>
-   <span data-ttu-id="d252a-800">Alle zwischen-K-Ebenen ohne gültigen CMY-Cube werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d252a-800">Any intermediate K level without a valid CMY cube will be ignored.</span></span>
-   <span data-ttu-id="d252a-801">Die CMY-Cubes verwenden möglicherweise nicht einheitliche Stichproben Intervalle (Raster Abstände), aber der gleiche Satz von Stichproben Intervallen muss in allen C-, M-und Y-Dimensionen des CMY-Cubes für eine bestimmte K-Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-801">The CMY cubes may use non-uniform sample intervals (grid spacing), but the same set of sample intervals must be used in all of the C,M, and Y dimensions in the CMY cube for a given K level.</span></span>
-   <span data-ttu-id="d252a-802">Jeder K-Level-CMY-Cube kann eine andere Anzahl und einen anderen Abstand von Beispiel Intervallen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d252a-802">Each K level CMY cube can use a different number and spacing of sample intervals.</span></span>
-   <span data-ttu-id="d252a-803">Alle CMY-Cubes müssen die "Ecken" des CMY-Cubes enthalten, d. h. CMY Samples bei \[ 0, 0, 0 \] , \[ 0, 0100 \] , \[ 0100, 0 \] , \[ 100, 0, 0 \] , \[ 0100.100 \] , \[ 100, 0100 \] , \[ 100.100, 0 \] , \[ 100.100.100 \] .</span><span class="sxs-lookup"><span data-stu-id="d252a-803">All CMY cubes must contain the "corners" of the CMY cube, that is, CMY samples at \[0,0,0\], \[0,0,100\], \[0,100,0\], \[100,0,0\], \[0,100,100\], \[100,0,100\], \[100,100, 0\], \[100,100,100\].</span></span>
-   <span data-ttu-id="d252a-804">Alle mittleren CMY-Raster Ebenen müssen in jedem Kanal vollständig abgetastet werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-804">Any intermediate CMY grid levels must be fully sampled in each channel.</span></span> <span data-ttu-id="d252a-805">Anders ausgedrückt: ein Beispiel muss bei jeder 3D-Raster Überschneidung innerhalb des CMY-Cubes vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d252a-805">In other words, a sample must exist at each 3-D grid intersection within the CMY cube.</span></span>
-   <span data-ttu-id="d252a-806">Für k = 0 und k = 100 CMY-Cubes sind 2 x 2x2-Cubes, die nur Ecken sind, als gültig akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d252a-806">For the K = 0 and K = 100 CMY cubes, 2x2x2 "corners-only" cubes are the minimum accepted as valid.</span></span>

    <span data-ttu-id="d252a-807">\[Hinweis: für k = 0 und k = 100 Ebenen wird ein 3x3x3-Cube als 2x2x2-Cube verarbeitet. die zwischen Abtast Ebene wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d252a-807">\[NOTE: for K=0 and K=100 levels, a 3x3x3 CMY cube will be processed as a 2x2x2 "corners-only" cube; the intermediate sample level is ignored.</span></span> <span data-ttu-id="d252a-808">für 4 x 4X4 und größere Cubes werden alle on-Grid-Beispiele verwendet.\]</span><span class="sxs-lookup"><span data-stu-id="d252a-808">4x4x4 and larger cubes will have all on-grid samples used.\]</span></span>

-   <span data-ttu-id="d252a-809">Für zwischen-K-Ebenen sind 4x4x4-CMY-Cubes die Mindestanzahl, die als gültig akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="d252a-809">For intermediate K levels, 4x4x4 CMY cubes are the minimum accepted as valid.</span></span>

<span data-ttu-id="d252a-810">Ein qualitativ hochwertiges Profil verwendet präzisere Stichproben Raster als das minimal erforderliche, das in der Regel 9x9x9x9 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="d252a-810">A high-quality profile will use finer sampling grids than the minimum required for validity, usually 9x9x9x9 or higher.</span></span> <span data-ttu-id="d252a-811">Die Beispiele der Ziele IT 8.7/3, IT 8.7/4 und ECI erstellen gültige Gerätemodell profile (DMPs) für das Gerätemodell des CMYK-druckerbaseline.</span><span class="sxs-lookup"><span data-stu-id="d252a-811">The samples from the IT8.7/3, IT8.7/4, and ECI targets produce valid device model profiles (DMPs)for the CMYK printer baseline device model.</span></span> <span data-ttu-id="d252a-812">Obwohl dieses Gerätemodell in der Lage ist, die überflüssigen (Off-Grid)-Beispiele in diesen Zielen zu ignorieren, ist es nicht garantiert, dass dies für andere Ziele möglich ist, und daher wird empfohlen, dass Sie aus maßsätzen entfernt werden, die in Profile für dieses Gerätemodell übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-812">While this device model is able to ignore the extraneous (off-grid) samples in these targets, it is not guaranteed to be able to do so for other targets, and so, it is recommended that extraneous samples be removed from measurement sets going into profiles for this device model.</span></span>

<span data-ttu-id="d252a-813">Die Inversion des Drucker Modells stellt weitere Schwierigkeiten dar.</span><span class="sxs-lookup"><span data-stu-id="d252a-813">The inversion of the printer model presents more difficulties.</span></span> <span data-ttu-id="d252a-814">Wenn eine Eingabe Farbe in ciecam vorliegt, gibt es eine Frage, ob sich diese Farbe im Drucker Spiel befindet.</span><span class="sxs-lookup"><span data-stu-id="d252a-814">Given an input color in CIECAM, there is a question of whether this color is within the printer gamut.</span></span> <span data-ttu-id="d252a-815">Außerdem gibt es das Problem bezüglich der Anordnung von Punkten im Farb Darstellungs Bereich.</span><span class="sxs-lookup"><span data-stu-id="d252a-815">There is also the issue regarding the arrangement of points in the color appearance space.</span></span> <span data-ttu-id="d252a-816">Die CMYK-Werte können zwar so angeordnet werden, dass Sie auf ein rechteckiges Raster fallen, wie dies im Ziel der IT-Version 8.7/3 der Fall ist. das gleiche gilt jedoch nicht für die sich ergebenden gedruckten Farben, da Sie sich im Raum der Farbdarstellung befinden.</span><span class="sxs-lookup"><span data-stu-id="d252a-816">While we can arrange the CMYK values to fall on a rectangular grid, as is done in the IT8.7/3 target, the same cannot be said of the resulting printed colors as they are situated in the color appearance space.</span></span> <span data-ttu-id="d252a-817">Im Allgemeinen sind Sie im Farb Darstellungs Raum ohne bestimmtes Muster verstreut.</span><span class="sxs-lookup"><span data-stu-id="d252a-817">In general, they are scattered in the color appearance space with no particular pattern.</span></span>

<span data-ttu-id="d252a-818">Im Allgemeinen gibt es zwei Ansätze für das Inversion-Problem von verstreuten Punkten.</span><span class="sxs-lookup"><span data-stu-id="d252a-818">There are generally two approaches to the inversion problem of scattered points.</span></span> <span data-ttu-id="d252a-819">Ein Ansatz besteht in der Verwendung einer geometrischen Unterteilung des Drucker Farbskala mithilfe von elementaren dreidimensionalen Festkörpern, wie z. b. "tetrahedra".</span><span class="sxs-lookup"><span data-stu-id="d252a-819">One approach is to use a geometric subdivision of the printer gamut using elementary 3-dimensional solids, such as tetrahedra.</span></span> <span data-ttu-id="d252a-820">Eine Unterteilung des Drucker Bereichs im Farb Darstellungs Bereich kann aus der entsprechenden unter Division des CMY-Speicherplatzes (K) abgeleitet werden. Weitere Informationen finden Sie unter nicht reagiert \[ 93 \] , Kang \[ 97 \] . Diese Vorgehensweise hat den Vorteil, dass die Einfachheit der Komplexität liegt.</span><span class="sxs-lookup"><span data-stu-id="d252a-820">A subdivision of the printer gamut in the color appearance space can be induced from the corresponding subdivision of the CMY(K) space, see Hung\[93\], Kang\[97\].This approach has the advantage of computational simplicity.</span></span> <span data-ttu-id="d252a-821">Im Fall eines Tetrahedron werden in einer Interpolations Weise nur vier Punkte verwendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-821">In the case of a tetrahedron, only four points are used in an interpolation.</span></span> <span data-ttu-id="d252a-822">Andererseits hängt das Ergebnis stark von einigen Punkten ab, was bedeutet, dass ein Messfehler eine bedeutende Auswirkung auf das Ergebnis hat.</span><span class="sxs-lookup"><span data-stu-id="d252a-822">On the other hand, the result depends heavily on a few points, which means that a measurement error will have a significant effect on the result.</span></span> <span data-ttu-id="d252a-823">Der interpolant ist auch tendenziell nicht so reibungslos.</span><span class="sxs-lookup"><span data-stu-id="d252a-823">The interpolant also tends to be not as smooth.</span></span> <span data-ttu-id="d252a-824">Der zweite Ansatz nimmt keine Unterteilung an und basiert auf der Technik der verstreuten Daten interpolung.</span><span class="sxs-lookup"><span data-stu-id="d252a-824">The second approach does not assume any subdivision, and is based on the technique of scattered data interpolation.</span></span> <span data-ttu-id="d252a-825">Ein klassisches Beispiel ist die Technik der Shepard-Interpolationsmethode oder eine umgekehrte gewichtete Methode (siehe Shepard \[ 68 \] ).</span><span class="sxs-lookup"><span data-stu-id="d252a-825">A classical example is the technique of Shepard interpolation, or inverse weighted method (See Shepard \[68\]).</span></span> <span data-ttu-id="d252a-826">Hier werden einige Punkte, die den Eingabe Punkt betreffen, auf irgendeine Weise ausgewählt, wobei jeder eine Gewichtung zugewiesen wird, in der Regel umgekehrt proportional zur Entfernung, und der interpolant als gewichteter Durchschnitt der benachbarten Punkte genommen wird.</span><span class="sxs-lookup"><span data-stu-id="d252a-826">Here, several points surrounding the input point are chosen in some manner, each assigned a weight, usually inversely proportional to the distance, and the interpolant is taken as the weighted average of the neighboring points.</span></span> <span data-ttu-id="d252a-827">Bei dieser Vorgehensweise ist die Wahl der benachbarten Punkte von entscheidender Bedeutung für die Leistung.</span><span class="sxs-lookup"><span data-stu-id="d252a-827">In this approach, the choice of neighboring points is paramount to performance.</span></span> <span data-ttu-id="d252a-828">Obwohl zu wenige Punkte den interpolanten ungenau und nicht glatt darstellen können, erzwingen zu viele Punkte eine hohe Rechenleistung, da die Gewichtungen in der Regel nichtlineare Funktionen sind und aufwändig berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-828">While too few points can render the interpolant inaccurate and non-smooth, too many points impose a high computational cost, as the weights are typically non-linear functions and costly to compute.</span></span>

<span data-ttu-id="d252a-829">Bei den beiden oben beschriebenen Ansätzen treten Probleme auf.</span><span class="sxs-lookup"><span data-stu-id="d252a-829">The two approaches described above both have problems.</span></span> <span data-ttu-id="d252a-830">Der Ansatz der Unterteilung hängt in der Regel von den Daten ab, die relativ reibungslos sind, und in der Regel ist der interpolant nicht sehr reibungslos.</span><span class="sxs-lookup"><span data-stu-id="d252a-830">The subdivision approach depends critically on the data being reasonably void of noise, and generally the interpolant is not very smooth.</span></span> <span data-ttu-id="d252a-831">Die verstreute Daten interpolung ist eher toleranter als das Daten Rauschen und sorgt im Allgemeinen für eine reibungslosere interpolante, aber Sie ist rechnerisch kostengünstiger.</span><span class="sxs-lookup"><span data-stu-id="d252a-831">The scattered data interpolation is more tolerant to data noise, and generally gives a smoother interpolant, but it is computationally more expensive.</span></span>

<span data-ttu-id="d252a-832">Der neue CTE hat einen alternativen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="d252a-832">The new CTE takes an alternative approach.</span></span> <span data-ttu-id="d252a-833">Das CMYK-Gerät wird als Sammlung von mehreren CMY-Geräten behandelt, von denen jeder einen bestimmten Wert Black (K) hat.</span><span class="sxs-lookup"><span data-stu-id="d252a-833">The CMYK device is treated as a collection of several CMY devices, each of which has a specific value of black (K).</span></span> <span data-ttu-id="d252a-834">Bei Verwendung eines Auswahl Algorithmus, der als Parameter Helligkeit und Chroma verwendet wird, wird eine schwarze Ebene ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d252a-834">Using a selection algorithm that takes as parameters lightness and chroma, a level of black is chosen.</span></span> <span data-ttu-id="d252a-835">Die CMY-Werte werden von der Inversion der entsprechenden CMY-zu Luv-Tabelle mithilfe der Newton-Methoden abgerufen, die an anderer Stelle vom RGB-Drucker Algorithmus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-835">The CMY values are obtained by inversion of the corresponding CMY to Luv table using the Newton methods employed elsewhere by the RGB printer algorithm.</span></span>

<span data-ttu-id="d252a-836">Führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="d252a-836">Use the following steps.</span></span>

1.  <span data-ttu-id="d252a-837">Drucken Sie das Ziel für die Charakterisierung, d. h. das Ziel "IT 8.7/3", oder ein Ziel, das eine Stichprobe des CMYK-Raums in regelmäßigen oder nicht regelmäßigen Abständen enthält.</span><span class="sxs-lookup"><span data-stu-id="d252a-837">Print the characterization target, which is either the IT8.7/3 target, or a target containing sampling of the CMYK space at regularly or irregularly spaced intervals.</span></span>
2.  <span data-ttu-id="d252a-838">Messen Sie das Ziel mithilfe eines spektrophoto meters, und konvertieren Sie die Messungen in CIELUV-Raum.</span><span class="sxs-lookup"><span data-stu-id="d252a-838">Measure the target using a spectrophotometer, and convert the measurements to CIELUV space.</span></span>
3.  <span data-ttu-id="d252a-839">Erstellen Sie die vorwärts Zuordnung von CMYK zu Luv.</span><span class="sxs-lookup"><span data-stu-id="d252a-839">Construct the forward map from CMYK to Luv.</span></span>
4.  <span data-ttu-id="d252a-840">Verwenden Sie die vorwärts Zuordnung, um einen Satz von CMY für Luv-Zuordnungen für einen Bereich von K-Werten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d252a-840">Use the forward map to construct a set of CMY to Luv maps for a range of K values.</span></span>
5.  <span data-ttu-id="d252a-841">Für jeden Eingabe-Luv-Wert wird der entsprechende CMYK-Wert abgerufen, indem eine der in Schritt 4 oben erstellten Zuordnungen ausgewählt und mit der-Methode von Newton zum Abrufen eines CMY Colorant-Satzes verwendet wird, der den ausgewählten K-Wert begleitet.</span><span class="sxs-lookup"><span data-stu-id="d252a-841">For any input Luv value, the corresponding CMYK value is obtained by selecting one of the maps constructed in step 4 above and inverting using Newton's method to obtain a CMY colorant set to accompany the K value selected.</span></span>

<span data-ttu-id="d252a-842">Die Schritte 1 und 2, bei denen es sich um Standardverfahren handelt, werden von einem Profil Erstellungs Programm ausgeführt, das nicht Teil des neuen CTE ist.</span><span class="sxs-lookup"><span data-stu-id="d252a-842">Steps 1 and 2, which are standard procedures, are performed by a profiling program that is not part of the new CTE.</span></span> <span data-ttu-id="d252a-843">Das Ziel "IT 8.7/3" enthält eine relativ detaillierte Stichprobe aller CMYK-Werte auf verschiedenen Ebenen von C, M, Y und k. Alternativ kann ein benutzerdefiniertes Ziel mit einheitlicher Stichprobenentnahme der C-, m-, y-und k-Kanäle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-843">The IT8.7/3 target contains a reasonably detailed sampling of all the CMYK values at various levels of C, M, Y, and K. Alternatively, a custom target with uniform sampling of the C, M, Y, and K channels can be used.</span></span> <span data-ttu-id="d252a-844">Nachdem das Ziel gedruckt wurde, kann ein "spektrophoto eter" oder ein "colormeter" verwendet werden, um den XYZ-Wert jedes Patches zu messen, und der XYZ-Wert kann mithilfe des CIELUV-Modells in den Luv-Wert konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-844">After the target is printed, a spectrophotometer or colorimeter can be used to measure the XYZ value of each patch, and the XYZ value can be converted to the Luv value using the CIELUV model.</span></span>

<span data-ttu-id="d252a-845">Schritt 3: die Konstruktion des vorwärts Bilds von CMYK zu Luv kann erreicht werden, indem alle bekannten Interpolations Techniken, wie z. b. "tetrahedral" oder "Multilinear", auf dem rechteckigen Raster im CMYK-Raum angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-845">Step 3, construction of the forward map from CMYK to Luv, can be achieved by applying any known interpolation technique, such as tetrahedral or multilinear method, on the rectangular grid in CMYK space.</span></span> <span data-ttu-id="d252a-846">Im neuen allgemeinen Tabellen Ausdruck wird eine 4-dimensionale tetrahedral-Interpolations Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="d252a-846">In the new CTE, a 4-dimensional tetrahedral interpolation is used.</span></span> <span data-ttu-id="d252a-847">Da sich die CMY-Samplings in der Regel auf jeder Ebene von K unterscheiden, verwenden wir eine Technik der Super-Stichprobenentnahme, wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d252a-847">Because the CMY sampling grids are generally different on each level of K, however, we use a technique of super-sampling, as detailed below.</span></span> <span data-ttu-id="d252a-848">Bei einem bestimmten CMYK-Punkt werden die k-Ebenen auf der Ebene zuerst basierend auf dem k-Wert bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d252a-848">For a given CMYK point, the sandwiching K levels are first determined based on the K value.</span></span> <span data-ttu-id="d252a-849">Führen Sie dann ein "Super Grid" auf jeder k-Ebene aus, bei der es sich um eine Kombination der CMY-Raster auf den beiden Ebenen handelt.</span><span class="sxs-lookup"><span data-stu-id="d252a-849">Then introduce a "super-grid" on each K level that is a union of the CMY grids on each of the two K levels.</span></span> <span data-ttu-id="d252a-850">Auf jeder k-Ebene wird der Luv-Wert jedes neu eingeführten Raster Punkts durch eine dreidimensionale, in dieser k-Ebene erstellbare multiinterpolations-Interpolations Stufe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d252a-850">On each K level, the Luv value of any newly introduced grid point is obtained by a 3-dimensional tetrahedral interpolation within that K level.</span></span> <span data-ttu-id="d252a-851">Zum Schluss wird eine 4-dimensionale tetrahedral-interpolung für den jeweiligen CMYK-Punkt in diesem neuen Raster ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d252a-851">Finally, a 4-dimensional tetrahedral interpolation for the specific CMYK point is performed on this new grid.</span></span>

![Diagramm, das Supersampling anzeigt.](images/cdmp-image163.png)

<span data-ttu-id="d252a-853">**Abbildung 8** : Supersampling</span><span class="sxs-lookup"><span data-stu-id="d252a-853">**Figure 8** : Supersampling</span></span>

<span data-ttu-id="d252a-854">In Schritt 4 wird eine Reihe von CMY-zu-Luv-Nachschlage Tabellen (LUTs) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d252a-854">Step 4 constructs a set of CMY-to-Luv lookup tables (LUTs).</span></span> <span data-ttu-id="d252a-855">Die in Schritt 3 erstellte vorwärts Zuordnung wird wiederholt aufgerufen, um den CMYK-Speicher neu zu testen.</span><span class="sxs-lookup"><span data-stu-id="d252a-855">The forward map constructed in Step 3 is called repeatedly to resample the CMYK space.</span></span> <span data-ttu-id="d252a-856">Der CMYK-Farbraum wird mit einem geraden Abstand von K und einem anderen, aber immer noch gleichmäßig belegten Sampling von CMY entnommen.</span><span class="sxs-lookup"><span data-stu-id="d252a-856">The CMYK color space is sampled using an even spacing of K and a different, but still evenly spaced, sampling of CMY.</span></span>

<span data-ttu-id="d252a-857">Schritt 5 ist ein Verfahren zum Abrufen des CMYK-Werts mithilfe der in Schritt 4 erstellten LUTs für jeden Eingabe-Luv-Punkt.</span><span class="sxs-lookup"><span data-stu-id="d252a-857">Step 5 is a procedure to obtain the CMYK value using the LUTs constructed in Step 4 for any input Luv point.</span></span> <span data-ttu-id="d252a-858">Der geeignete Wert von K wird ausgewählt, indem die Helligkeit und der Grad der Farbe in der angeforderten Luv analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-858">The appropriate value of K is chosen by analyzing the lightness as well as the degree of color in the Luv requested.</span></span> <span data-ttu-id="d252a-859">Nachdem die Tabelle ausgewählt wurde, werden die CMY-Werte mithilfe der Newton-Methode aus der Tabelle abgerufen (wie zuvor unter dem RGB-Drucker Gerätemodell dokumentiert).</span><span class="sxs-lookup"><span data-stu-id="d252a-859">After the table is selected, the CMY values are obtained from the table by using Newton's method (as documented under the RGB printer device model earlier).</span></span>

<span data-ttu-id="d252a-860">Der CIELUV-Speicherplatz wird im Drucker Modell anstelle von ciejab verwendet, da das Gerätemodell ausschließlich auf den im DMP verfügbaren farbmetrikdaten basieren soll.</span><span class="sxs-lookup"><span data-stu-id="d252a-860">CIELUV space is used in the printer model instead of CIEJab because the device model should be based solely on colorimetric data available in the DMP.</span></span> <span data-ttu-id="d252a-861">Das DMP enthält farbige Metrikdaten für jeden gemessenen Patch, einschließlich des Medien weißen Punkts. Daher ist es möglich, CIEXYZ-Daten in CIELUV-Daten zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="d252a-861">The DMP contains colorimetric data for each measured patch, including the media white point, so it is possible to convert CIEXYZ data into CIELUV data.</span></span> <span data-ttu-id="d252a-862">Es ist jedoch nicht möglich, in CIECAM02 Jch oder Jab zu konvertieren, da es keinen Zugriff auf die Informationen in der Anzeige Bedingung in der DMP gibt.</span><span class="sxs-lookup"><span data-stu-id="d252a-862">However, it is not possible to convert to CIECAM02 JCh or Jab, because there is no access to the viewing condition information in the DMP.</span></span>

### <a name="rgb-projector-device-model-baseline"></a><span data-ttu-id="d252a-863">Basislinie des RGB-projektorgeräts</span><span class="sxs-lookup"><span data-stu-id="d252a-863">RGB Projector Device Model Baseline</span></span>

<span data-ttu-id="d252a-864">Hinweis: viele RGB-Projektoren haben mehr als einen Betriebsmodus.</span><span class="sxs-lookup"><span data-stu-id="d252a-864">Note: Many RGB projectors have more than one operating mode.</span></span> <span data-ttu-id="d252a-865">In einem Modus, bei dem es sich oft um die Standardeinstellung handelt, die beispielsweise als "Präsentation" bezeichnet werden kann, wird die Farb Antwort des Projektor für maximale Helligkeit optimiert.</span><span class="sxs-lookup"><span data-stu-id="d252a-865">In one mode, which is often the default and might be called something like "presentation," the color response of the projector is optimized for maximum brightness.</span></span> <span data-ttu-id="d252a-866">In diesem Modus verliert der Projektor jedoch die Möglichkeit, helle und leicht zu verächende Farben (z. b. blendtöne und einige fleischfarben) zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="d252a-866">However, in this mode, the projector loses the ability to reproduce light, slightly chromatic colors such as pale yellows and some flesh tones.</span></span> <span data-ttu-id="d252a-867">Der Projektor ist in einem anderen Modus, der häufig als "Film", "Video" oder "sRGB" bezeichnet wird, für die Reproduktion realistischer Bilder und natürlicher Szenen optimiert.</span><span class="sxs-lookup"><span data-stu-id="d252a-867">In another mode, often called "film," "video," or "sRGB," the projector is optimized for reproduction of realistic images and natural scenes.</span></span> <span data-ttu-id="d252a-868">In diesem Modus wird die maximale Helligkeit abgehandelt, um die Gesamtqualität der Farb Reproduktion zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d252a-868">In this mode, maximum brightness is traded off to improve the overall quality of the color reproduction.</span></span> <span data-ttu-id="d252a-869">Um eine zufriedenstellende Farb Reproduktion mit RGB-Projektoren zu erhalten, ist es erforderlich, den Projektor in einem Modus zu platzieren, in dem eine Glättung von Farben wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d252a-869">To obtain satisfactory color reproduction with RGB projectors, it is necessary to place the projector in a mode where a smooth gamut of colors can be reproduced.</span></span>

![Diagramm mit einem D L P-Gerätemodell.](images/cdmp-image167.png)

<span data-ttu-id="d252a-871">**Abbildung 9** : DLP-Gerätemodell</span><span class="sxs-lookup"><span data-stu-id="d252a-871">**Figure 9** : DLP device model</span></span>

<span data-ttu-id="d252a-872">Ein eingehender RGB-Wert übergibt zwei Berechnungs Pfade.</span><span class="sxs-lookup"><span data-stu-id="d252a-872">An incoming RGB value passes through two computational pathways.</span></span> <span data-ttu-id="d252a-873">Der erste ist das Matrix Modell, das zu einem XYZ-Wert führt.</span><span class="sxs-lookup"><span data-stu-id="d252a-873">The first is the matrix model, which results in an XYZ value.</span></span> <span data-ttu-id="d252a-874">Danach folgt die Konvertierung von XYZ in Luv.</span><span class="sxs-lookup"><span data-stu-id="d252a-874">This is immediately followed by the conversion from XYZ to Luv.</span></span> <span data-ttu-id="d252a-875">Die zweite ist die nicht einheitliche LUT-interpolung mit der tetrahedral-interpolung.</span><span class="sxs-lookup"><span data-stu-id="d252a-875">The second is the non-uniform LUT interpolation using tetrahedral interpolation.</span></span> <span data-ttu-id="d252a-876">Die Ausgabe der Interpolation befindet sich bereits im Luv-Raum durch Konstruktion.</span><span class="sxs-lookup"><span data-stu-id="d252a-876">The output of the interpolation is already in Luv space by construction.</span></span> <span data-ttu-id="d252a-877">Die beiden Ausgaben werden hinzugefügt, um den vorhergesagten Luv-Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d252a-877">The two outputs are added to obtain the predicted Luv value.</span></span> <span data-ttu-id="d252a-878">Diese wird schließlich in XYZ konvertiert. Dies ist die erwartete Ausgabe des Farb Metrik Modells für das DLP-Gerät.</span><span class="sxs-lookup"><span data-stu-id="d252a-878">This is finally converted to XYZ, which is the expected output of the colorimetric model for the DLP device.</span></span>

<span data-ttu-id="d252a-879">Da Projektoren Geräte anzeigen, unterstützen Sie auch die Inversion des Modells, d. h. die Transformation von XYZ zu RGB.</span><span class="sxs-lookup"><span data-stu-id="d252a-879">Since projectors are display devices, they also support the inversion of the model, that is, the transform from XYZ to RGB.</span></span> <span data-ttu-id="d252a-880">Da das Gerätemodell RGB-Speicherplatz in XYZ-Leerraum umwandelt, bei dem es sich um dreidimensionale handelt, entspricht Inversion der Behebung von drei nichtlinearen Gleichungen in drei unbekannten Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d252a-880">Because the device model transforms RGB space to XYZ space, which are both three dimensional, inversion is equivalent to solving three nonlinear equations in three unknowns.</span></span> <span data-ttu-id="d252a-881">Dies kann durch standardmäßige Formel-und Lösungsverfahren wie Newton-Raphson erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="d252a-881">This can done by standard equation solving techniques, such as Newton-Raphson.</span></span> <span data-ttu-id="d252a-882">Es ist jedoch vorzuziehen, zuerst XYZ in Luv zu konvertieren und dann die Luv in RGB-Transformation umzukehren, da der Luv-Speicher eher perperer linear ist als XYZ-Leerraum.</span><span class="sxs-lookup"><span data-stu-id="d252a-882">It is preferable, however, to first convert XYZ to Luv, and then invert the Luv To RGB transform, because Luv space is more perceptually linear than XYZ space.</span></span>

### <a name="icc-device-model-baseline"></a><span data-ttu-id="d252a-883">Basislinie des Modells für das Modell</span><span class="sxs-lookup"><span data-stu-id="d252a-883">ICC Device Model Baseline</span></span>

<span data-ttu-id="d252a-884">Die Initialisierungsfunktion für den Workflow des Workflows wird durch Erstellen eines speziellen Gerätemodell Profils für das ICC-Gerät aktiviert, das das Profil Objekt speichert und eine ICC-Transformation mit einem No-op XYZ-Profil erstellt.</span><span class="sxs-lookup"><span data-stu-id="d252a-884">The CITE ICC workflow interoperability is enabled by creating a special ICC device baseline device model profile that stores the profile object and creates a ICC transform using a no-op XYZ profile.</span></span> <span data-ttu-id="d252a-885">Diese Transformation wird dann verwendet, um zwischen Geräte-und CIEXYZ-Farben zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="d252a-885">This transform is then used to translate between device and CIEXYZ colors.</span></span>

![Das Diagramm zeigt die Interoperabilität zwischen c i T E i c c-Workflow.](images/cdmp-image168.png)

<span data-ttu-id="d252a-887">**Abbildung 10** : zitieren der Interoperabilität von Workflow Workflows</span><span class="sxs-lookup"><span data-stu-id="d252a-887">**Figure 10** : CITE ICC Workflow Interoperability</span></span>

## <a name="related-topics"></a><span data-ttu-id="d252a-888">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d252a-888">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d252a-889">Konzepte der grundlegenden Farbverwaltung</span><span class="sxs-lookup"><span data-stu-id="d252a-889">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="d252a-890">Windows Color System: Schemas und Algorithmen</span><span class="sxs-lookup"><span data-stu-id="d252a-890">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





