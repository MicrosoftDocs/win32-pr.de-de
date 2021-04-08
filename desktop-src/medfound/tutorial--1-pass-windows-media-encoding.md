---
description: 'Codierung bezieht sich auf den Prozess der Umstellung digitaler Medien von einem Format in ein anderes. Beispiel: das Umrechnen von MP3-Audiodaten in Windows Media Audio Format gemäß der Definition des Advanced Systems Format (ASF).'
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: 'Tutorial: 1-Pass-Windows-Medien Codierung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761460"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a><span data-ttu-id="aee28-104">Tutorial: 1-Pass-Windows-Medien Codierung</span><span class="sxs-lookup"><span data-stu-id="aee28-104">Tutorial: 1-Pass Windows Media Encoding</span></span>

<span data-ttu-id="aee28-105">Codierung bezieht sich auf den Prozess der Umstellung digitaler Medien von einem Format in ein anderes.</span><span class="sxs-lookup"><span data-stu-id="aee28-105">Encoding refers to the process of converting digital media from one format into another.</span></span> <span data-ttu-id="aee28-106">Beispiel: das Umrechnen von MP3-Audiodaten in Windows Media Audio Format gemäß der Definition des Advanced Systems Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="aee28-106">For example, converting MP3 audio into Windows Media Audio format as defined by the Advanced Systems Format (ASF) specification.</span></span>

<span data-ttu-id="aee28-107">**Hinweis**  Die ASF-Spezifikation definiert einen Containertyp für die Ausgabedatei (. WMA oder. wmv), die Mediendaten in einem beliebigen Format enthalten kann, komprimiert oder unkomprimiert.</span><span class="sxs-lookup"><span data-stu-id="aee28-107">**Note**  The ASF specification defines a container type for the output file (.wma or .wmv) that can contain media data in any format, compressed or uncompressed.</span></span> <span data-ttu-id="aee28-108">Beispielsweise kann ein ASF-Container, z. b. eine. WMA-Datei, Mediendaten im MP3-Format enthalten.</span><span class="sxs-lookup"><span data-stu-id="aee28-108">For example, an ASF container such as a .wma file can contain media data in MP3 format.</span></span> <span data-ttu-id="aee28-109">Beim Codierungsprozess wird das tatsächliche Format der in der Datei enthaltenen Daten konvertiert.</span><span class="sxs-lookup"><span data-stu-id="aee28-109">The encoding process converts the actual format of the data contained within the file.</span></span>

<span data-ttu-id="aee28-110">In diesem Tutorial wird veranschaulicht, wie Sie die Eingabe Quelle für unverschlüsselte Inhalte (nicht DRM-geschützt) in Windows Media-Inhalt codieren und die Daten in einer neuen ASF-Datei (. WM \* ) mithilfe von ASF-Komponenten der Pipeline Schicht schreiben</span><span class="sxs-lookup"><span data-stu-id="aee28-110">This tutorial demonstrates encoding clear content (non DRM-protected) input source into Windows Media content and writing the data in a new ASF file (.wm\*) by using Pipeline Layer ASF Components.</span></span> <span data-ttu-id="aee28-111">Diese Komponenten werden verwendet, um eine partielle Codierungs Topologie zu erstellen, die von einer Instanz der Medien Sitzung gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-111">These components will be used to build a partial encoding topology, which will be controlled by an instance of the Media Session.</span></span>

<span data-ttu-id="aee28-112">In diesem Tutorial erstellen Sie eine Konsolenanwendung, die die Dateinamen für die Eingabe und Ausgabe und den Codierungs Modus als Argumente annimmt.</span><span class="sxs-lookup"><span data-stu-id="aee28-112">In this tutorial, you will create a console application that takes the input and output filenames, and the encoding mode as arguments.</span></span> <span data-ttu-id="aee28-113">Die Eingabedatei kann ein komprimiertes oder ein nicht komprimiertes Medienformat aufweisen.</span><span class="sxs-lookup"><span data-stu-id="aee28-113">The input file can be in a compressed or an uncompressed media format.</span></span> <span data-ttu-id="aee28-114">Gültige Codierungs Modi sind "CBR" (Konstante Bitrate) oder "VBR" (Variable Bitrate).</span><span class="sxs-lookup"><span data-stu-id="aee28-114">The valid encoding modes are "CBR" (constant bit rate) or "VBR" (variable bit rate).</span></span> <span data-ttu-id="aee28-115">Die Anwendung erstellt eine Medienquelle, die die durch den Eingabe Dateinamen angegebene Quelle darstellt, und die ASF-Datei-Senke, um den codierten Inhalt der Quelldatei in einer ASF-Datei zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="aee28-115">The application creates a media source to represent the source specified by the input filename, and the ASF file sink to archive the encoded contents of source file into an ASF file.</span></span> <span data-ttu-id="aee28-116">Damit das Szenario einfach implementiert werden kann, verfügt die Ausgabedatei nur über einen Audiostream und einen Videostream.</span><span class="sxs-lookup"><span data-stu-id="aee28-116">To keep the scenario simple to implement, the output file will have only one audio stream and one video stream.</span></span> <span data-ttu-id="aee28-117">Die Anwendung fügt den Windows Media Audio 9,1 Professional-Codec für die Audiostream-Formatkonvertierung und Windows Media Video 9-Codec für den Videostream ein.</span><span class="sxs-lookup"><span data-stu-id="aee28-117">The application inserts the Windows Media Audio 9.1 Professional codec for the audio stream format conversion and Windows Media Video 9 codec for the video stream.</span></span>

<span data-ttu-id="aee28-118">Bei konstanter Bitrate-Codierung muss der Encoder vor Beginn der Codierungs Sitzung die Zielbitrate kennen, die er erreichen muss.</span><span class="sxs-lookup"><span data-stu-id="aee28-118">For constant bit rate encoding, before the encoding session begins, the encoder must know the target bit rate that it must achieve.</span></span> <span data-ttu-id="aee28-119">In diesem Tutorial verwendet die Anwendung für den Modus "CBR" die Bitrate, die mit dem ersten Ausgabe Medientyp verfügbar ist, der vom Encoder während der Medientyp Aushandlung als Zielbitrate abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-119">In this tutorial, for "CBR" mode, the application uses the bit rate available with the first output media type that is retrieved from the encoder during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="aee28-120">Für die variablenbitrate-Codierung veranschaulicht dieses Tutorial die Codierung mit variabler Bitrate durch Festlegen einer Qualitätsstufe.</span><span class="sxs-lookup"><span data-stu-id="aee28-120">For variable bit rate encoding, this tutorial demonstrates encoding with variable bit rate by setting a quality level.</span></span> <span data-ttu-id="aee28-121">Die Audiodatenströme werden auf der Qualitätsstufe 98 und Videostreams auf der Qualitätsstufe 95 codiert.</span><span class="sxs-lookup"><span data-stu-id="aee28-121">The audio streams are encoded at the quality level of 98 and video streams at the quality level of 95.</span></span>

<span data-ttu-id="aee28-122">Im folgenden Verfahren werden die Schritte zum Codieren von Windows Media-Inhalten in einem ASF-Container mithilfe eines 1-Pass-Codierungs Modus zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="aee28-122">The following procedure summarizes the steps for encoding Windows Media content in an ASF container by using a 1-pass encoding mode.</span></span>

1.  <span data-ttu-id="aee28-123">Erstellen Sie eine Medienquelle für die angegebene mithilfe des Quell Resolvers.</span><span class="sxs-lookup"><span data-stu-id="aee28-123">Create a media source for the specified by using the source resolver.</span></span>
2.  <span data-ttu-id="aee28-124">Listet die Streams in der Medienquelle auf.</span><span class="sxs-lookup"><span data-stu-id="aee28-124">Enumerate the streams in the media source.</span></span>
3.  <span data-ttu-id="aee28-125">Erstellen Sie die ASF-Medien Senke, und fügen Sie in Abhängigkeit von den Streams in der Medienquelle, die codiert werden müssen, streamsenken hinzu.</span><span class="sxs-lookup"><span data-stu-id="aee28-125">Create the ASF media sink and add stream sinks depending on the streams in the media source that need to be encoded.</span></span>
4.  <span data-ttu-id="aee28-126">Konfigurieren Sie die Medien Senke mit den erforderlichen Codierungs Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aee28-126">Configure the media sink with the required encoding properties.</span></span>
5.  <span data-ttu-id="aee28-127">Erstellen Sie die Windows Media Encoder für die Streams in der Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="aee28-127">Create the Windows Media encoders for the streams in the output file.</span></span>
6.  <span data-ttu-id="aee28-128">Konfigurieren Sie die Encoder mit den Eigenschaften, die für die Medien Senke festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="aee28-128">Configure the encoders with the properties that are set on the media sink.</span></span>
7.  <span data-ttu-id="aee28-129">Erstellen Sie eine partielle Codierungs Topologie.</span><span class="sxs-lookup"><span data-stu-id="aee28-129">Build a partial encoding topology.</span></span>
8.  <span data-ttu-id="aee28-130">Instanziieren Sie die Medien Sitzung, und legen Sie die Topologie für die Medien Sitzung fest.</span><span class="sxs-lookup"><span data-stu-id="aee28-130">Instantiate the Media Session and set the topology on the Media Session.</span></span>
9.  <span data-ttu-id="aee28-131">Starten Sie die Codierungs Sitzung, indem Sie die Medien Sitzung Steuern und alle relevanten Ereignisse aus der Medien Sitzung erhalten.</span><span class="sxs-lookup"><span data-stu-id="aee28-131">Start the encoding session by controlling the Media Session and getting all the relevant events from the Media Session.</span></span>
10. <span data-ttu-id="aee28-132">Bei der VBR-Codierung werden die Codierungs Eigenschaftswerte aus dem Encoder und auf der Medien Senke festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aee28-132">For VBR encoding, get the encoding property values from the encoder and set them on the media sink.</span></span>
11. <span data-ttu-id="aee28-133">Schließen und beenden Sie die Codierungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="aee28-133">Close and shutdown the encoding session.</span></span>

<span data-ttu-id="aee28-134">Dieses Tutorial enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="aee28-134">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="aee28-135">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="aee28-135">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="aee28-136">Einrichten des Projekts</span><span class="sxs-lookup"><span data-stu-id="aee28-136">Set up the Project</span></span>](#set-up-the-project)
-   [<span data-ttu-id="aee28-137">Erstellen der Medienquelle</span><span class="sxs-lookup"><span data-stu-id="aee28-137">Create the Media Source</span></span>](#create-the-media-source)
-   [<span data-ttu-id="aee28-138">Erstellen der ASF-Datei-Senke</span><span class="sxs-lookup"><span data-stu-id="aee28-138">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
    -   [<span data-ttu-id="aee28-139">Erstellen des ASF-Profil Objekts</span><span class="sxs-lookup"><span data-stu-id="aee28-139">Create the ASF Profile Object</span></span>](#create-the-asf-profile-object)
    -   [<span data-ttu-id="aee28-140">Erstellen eines komprimierten Audiomedien Typs</span><span class="sxs-lookup"><span data-stu-id="aee28-140">Create a Compressed Audio Media Type</span></span>](#create-a-compressed-audio-media-type)
    -   [<span data-ttu-id="aee28-141">Erstellen eines komprimierten Video Medientyps</span><span class="sxs-lookup"><span data-stu-id="aee28-141">Create a Compressed Video Media Type</span></span>](#create-a-compressed-video-media-type)
    -   [<span data-ttu-id="aee28-142">Erstellen des ASF-ContentInfo-Objekts</span><span class="sxs-lookup"><span data-stu-id="aee28-142">Create the ASF ContentInfo Object</span></span>](#create-the-asf-contentinfo-object)
    -   [<span data-ttu-id="aee28-143">Erstellen der ASF-Datei-Senke</span><span class="sxs-lookup"><span data-stu-id="aee28-143">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
-   [<span data-ttu-id="aee28-144">Erstellen der partiellen Codierungs Topologie</span><span class="sxs-lookup"><span data-stu-id="aee28-144">Build the Partial Encoding Topology</span></span>](#build-the-partial-encoding-topology)
    -   [<span data-ttu-id="aee28-145">Erstellen des Knotens "Quell Topologie" für die Medienquelle</span><span class="sxs-lookup"><span data-stu-id="aee28-145">Create the Source Topology Node for the Media Source</span></span>](#create-the-source-topology-node-for-the-media-source)
    -   [<span data-ttu-id="aee28-146">Instanziieren Sie die erforderlichen Encoder, und erstellen Sie die Transformations Knoten.</span><span class="sxs-lookup"><span data-stu-id="aee28-146">Instantiate the Required Encoders and Create the Transform Nodes</span></span>](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [<span data-ttu-id="aee28-147">Erstellen der Knoten für die Ausgabe Topologie für die Datei Senke</span><span class="sxs-lookup"><span data-stu-id="aee28-147">Create the Output Topology Nodes for the File Sink</span></span>](#create-the-output-topology-nodes-for-the-file-sink)
    -   [<span data-ttu-id="aee28-148">Verbinden der Quell-, Transformations-und Senke Knoten</span><span class="sxs-lookup"><span data-stu-id="aee28-148">Connect the Source, Transform, and Sink Nodes</span></span>](#connect-the-source-transform-and-sink-nodes)
-   [<span data-ttu-id="aee28-149">Verarbeiten der Codierungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="aee28-149">Handling the Encoding Session</span></span>](#handling-the-encoding-session)
-   [<span data-ttu-id="aee28-150">Aktualisieren der Codierungs Eigenschaften in der Datei Senke</span><span class="sxs-lookup"><span data-stu-id="aee28-150">Update Encoding Properties in the File Sink</span></span>](#update-encoding-properties-in-the-file-sink)
-   [<span data-ttu-id="aee28-151">Implementieren von Main</span><span class="sxs-lookup"><span data-stu-id="aee28-151">Implement Main</span></span>](#implement-main)
-   [<span data-ttu-id="aee28-152">Testen der Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="aee28-152">Test the Output File</span></span>](#test-the-output-file)
-   [<span data-ttu-id="aee28-153">Allgemeine Fehler Codes und Tipps zum Debuggen</span><span class="sxs-lookup"><span data-stu-id="aee28-153">Common Error Codes and Debugging Tips</span></span>](#common-error-codes-and-debugging-tips)
-   [<span data-ttu-id="aee28-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aee28-154">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="aee28-155">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="aee28-155">Prerequisites</span></span>

<span data-ttu-id="aee28-156">In diesem Tutorial wird Folgendes vorausgesetzt:</span><span class="sxs-lookup"><span data-stu-id="aee28-156">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="aee28-157">Sie sind mit der [ASF-Dateistruktur](asf-file-structure.md)vertraut, die von Media Foundation bereitgestellten [ASF-Komponenten der Pipeline Schicht](pipeline-layer-asf-components.md) , um mit ASF-Objekten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="aee28-157">You are familiar with the [ASF File Structure](asf-file-structure.md), the [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="aee28-158">Zu diesen Komponenten gehören die folgenden Objekte:</span><span class="sxs-lookup"><span data-stu-id="aee28-158">These components include the following objects:</span></span>
    -   [<span data-ttu-id="aee28-159">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="aee28-159">Media Sources</span></span>](media-sources.md)

        <span data-ttu-id="aee28-160">**Hinweis**  Wenn Sie die transbewertung durchführen (das Umwandeln einer höheren Bitrate-Datei in eine Datei mit niedrigerer Bitrate ohne Änderung von Formaten), verwenden Sie die [ASF-Medienquelle](asf-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-160">**Note**  If you are performing transrating (converting a higher bit-rate file to a lower bit-rate file without changing formats), you will use the [ASF Media Source](asf-media-source.md).</span></span>

    -   [<span data-ttu-id="aee28-161">Windows Media Encoder</span><span class="sxs-lookup"><span data-stu-id="aee28-161">Windows Media Encoders</span></span>](windows-media-encoders.md)
    -   [<span data-ttu-id="aee28-162">ASF-Medien senken</span><span class="sxs-lookup"><span data-stu-id="aee28-162">ASF Media Sinks</span></span>](asf-media-sinks.md)
    -   [<span data-ttu-id="aee28-163">ASF-ContentInfo-Objekt</span><span class="sxs-lookup"><span data-stu-id="aee28-163">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
    -   [<span data-ttu-id="aee28-164">ASF-Profil</span><span class="sxs-lookup"><span data-stu-id="aee28-164">ASF Profile</span></span>](asf-profile.md)

-   <span data-ttu-id="aee28-165">Sie sind mit Windows Media Encoder und den verschiedenen Codierungs Typen vertraut, insbesondere [konstanter Bitraten Codierung](constant-bit-rate-encoding.md) und [Qualitäts basierter variablenbitrate-Codierung](quality-based-variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-165">You are familiar with Windows Media encoders, and the various encoding types, particularly [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) and [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md).</span></span>
-   <span data-ttu-id="aee28-166">Sie sind mit MFT-Codierungs Vorgängen vertraut.</span><span class="sxs-lookup"><span data-stu-id="aee28-166">You are familiar with encoder MFT operations.</span></span> <span data-ttu-id="aee28-167">Insbesondere das Erstellen einer Instanz des Encoders und das Festlegen von Eingabe-und Ausgabetypen für den Encoder.</span><span class="sxs-lookup"><span data-stu-id="aee28-167">Specifically, creating an instance of the encoder and setting input and output types on the encoder.</span></span>
-   <span data-ttu-id="aee28-168">Sie sind mit Topologieobjekten vertraut und erfahren, wie Sie eine Codierungs Topologie erstellen.</span><span class="sxs-lookup"><span data-stu-id="aee28-168">You are familiar with topology objects and how to build an encoding topology.</span></span> <span data-ttu-id="aee28-169">Weitere Informationen zu Topologien und topologieknoten finden Sie unter [Erstellen von Topologien](creating-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-169">For more information about topologies and topology nodes, see [Creating Topologies](creating-topologies.md).</span></span>
-   <span data-ttu-id="aee28-170">Sie sind mit dem Ereignis Modell der [Medien Sitzung](media-session.md)und den Fluss Steuerungs Vorgängen vertraut.</span><span class="sxs-lookup"><span data-stu-id="aee28-170">You are familiar with [Media Session](media-session.md)'s event model and the flow control operations.</span></span> <span data-ttu-id="aee28-171">Weitere Informationen finden Sie unter [Medien Sitzungs Ereignisse](media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-171">For information, see [Media Session Events](media-session-events.md).</span></span>

## <a name="set-up-the-project"></a><span data-ttu-id="aee28-172">Einrichten des Projekts</span><span class="sxs-lookup"><span data-stu-id="aee28-172">Set up the Project</span></span>

1.  <span data-ttu-id="aee28-173">Fügen Sie die folgenden Header in die Quelldatei ein:</span><span class="sxs-lookup"><span data-stu-id="aee28-173">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  <span data-ttu-id="aee28-174">Verknüpfen Sie die folgenden Bibliotheksdateien:</span><span class="sxs-lookup"><span data-stu-id="aee28-174">Link to the following library files:</span></span>

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  <span data-ttu-id="aee28-175">Deklarieren Sie die Funktion [saferelease](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="aee28-175">Declare the [SafeRelease](saferelease.md) function.</span></span>

    ```C++
    template <class T> void SafeRelease(T **ppT)
    {
        if (*ppT)
        {
            (*ppT)->Release();
            *ppT = NULL;
        }
    }
    ```

    

4.  <span data-ttu-id="aee28-176">Deklarieren Sie die Codierungs \_ Modus-Enumeration zum Definieren von CBR-und VBR-Codierungs Typen</span><span class="sxs-lookup"><span data-stu-id="aee28-176">Declare the ENCODING\_MODE enumeration to define CBR and VBR encoding types.</span></span>

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  <span data-ttu-id="aee28-177">Definiert eine Konstante für das Puffer Fenster für einen Videostream.</span><span class="sxs-lookup"><span data-stu-id="aee28-177">Define a constant for buffer window for a video stream.</span></span>

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a><span data-ttu-id="aee28-178">Erstellen der Medienquelle</span><span class="sxs-lookup"><span data-stu-id="aee28-178">Create the Media Source</span></span>

<span data-ttu-id="aee28-179">Erstellen Sie eine Medienquelle für die Eingabe Quelle.</span><span class="sxs-lookup"><span data-stu-id="aee28-179">Create a media source for the input source.</span></span> <span data-ttu-id="aee28-180">Media Foundation stellt integrierte Medienquellen für verschiedene Medienformate bereit: MP3, MP4/3GP, AVI/Wave.</span><span class="sxs-lookup"><span data-stu-id="aee28-180">Media Foundation provides built-in media sources for various media formats: MP3, MP4/3GP, AVI/WAVE.</span></span> <span data-ttu-id="aee28-181">Informationen zu den von Media Foundation unterstützten Formaten finden Sie [unter Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-181">For information about the formats supported by Media Foundation, see [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).</span></span>

<span data-ttu-id="aee28-182">Verwenden Sie zum Erstellen der Medienquelle den [quellresolver](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-182">To create the media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="aee28-183">Dieses Objekt analysiert die URL, die für die Quelldatei angegeben wurde, und erstellt die entsprechende Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="aee28-183">This object analyzes the URL that was specified for the source file and creates the appropriate media source.</span></span>

<span data-ttu-id="aee28-184">Führen Sie die folgenden Aufrufe aus:</span><span class="sxs-lookup"><span data-stu-id="aee28-184">Make the following calls:</span></span>

-   [<span data-ttu-id="aee28-185">**MF | atesourceresolver**</span><span class="sxs-lookup"><span data-stu-id="aee28-185">**MFCreateSourceResolver**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [<span data-ttu-id="aee28-186">**IMF sourceresolver:: forateobjectfromurl**</span><span class="sxs-lookup"><span data-stu-id="aee28-186">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    <span data-ttu-id="aee28-187">Weitere Informationen zu diesen Aufrufen finden Sie unter [using the Source Resolver](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-187">For more information about these calls, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

    <span data-ttu-id="aee28-188">Wenn die Eingabedatei im ASF-Format vorliegt und Sie Sie in eine andere Bitrate Datei konvertieren möchten, ohne Formate zu ändern, erstellt der Quell-Solver eine Instanz der [ASF-Medienquelle](asf-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-188">If your input file is in ASF format and you want to convert it to a different bit-rate file without changing formats, the source solver creates an instance of the [ASF Media Source](asf-media-source.md).</span></span>

<span data-ttu-id="aee28-189">Das folgende Codebeispiel zeigt eine Funktion, die für die angegebene Datei eine Medienquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="aee28-189">The following code example shows a function CreateMediaSource that creates a media source for the specified file.</span></span>


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a><span data-ttu-id="aee28-190">Erstellen der ASF-Datei-Senke</span><span class="sxs-lookup"><span data-stu-id="aee28-190">Create the ASF File Sink</span></span>

<span data-ttu-id="aee28-191">Erstellen Sie eine Instanz der ASF-Datei-Senke, die codierte Mediendaten in einer ASF-Datei am Ende der Codierungs Sitzung archiviert.</span><span class="sxs-lookup"><span data-stu-id="aee28-191">Create an instance of the ASF file sink that will archive encoded media data to an ASF file at the end of the encoding session.</span></span>

<span data-ttu-id="aee28-192">In diesem Tutorial erstellen Sie ein Aktivierungs Objekt für die ASF-Datei-Senke.</span><span class="sxs-lookup"><span data-stu-id="aee28-192">In this tutorial, you will create an activation object for the ASF file sink.</span></span> <span data-ttu-id="aee28-193">Die dateisenke benötigt die folgenden Informationen, um die erforderlichen streamsenken zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aee28-193">The file sink needs the following information in order to create the required stream sinks.</span></span>

-   <span data-ttu-id="aee28-194">Die Streams, die codiert und in die endgültige Datei geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aee28-194">The streams to be encoded and written in the final file.</span></span>
-   <span data-ttu-id="aee28-195">Die Codierungs Eigenschaften, die zum Codieren des Medien Inhalts verwendet werden, z. b. Codierungstyp, Anzahl der Codierungs Durchläufen und die zugehörigen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aee28-195">The encoding properties that are used to encode the media content, such as, type of encoding, number of encoding passes, and the related properties.</span></span>
-   <span data-ttu-id="aee28-196">Die globalen Dateieigenschaften, die für die Medien Senke angeben, ob die Parameter für die Leaky-Bucket (Bitrate und Puffergröße) automatisch angepasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aee28-196">The global file properties that indicate to the media sink whether it should adjust the leaky bucket parameters (bit rate and buffer size) automatically.</span></span>

<span data-ttu-id="aee28-197">Die Datenstrom Informationen werden im ASF-Profil Objekt konfiguriert, und die Codierungs-und globalen Eigenschaften werden in einem Eigenschaften Speicher festgelegt, der vom ASF-ContentInfo-Objekt verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-197">The stream information is configured in the ASF Profile object and the encoding and global properties are set in a property store managed by the ASF ContentInfo Object.</span></span>

<span data-ttu-id="aee28-198">Eine Übersicht über die ASF-Datei-Senke finden Sie unter [ASF-Medien senken](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-198">For an overview of the ASF file sink, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

### <a name="create-the-asf-profile-object"></a><span data-ttu-id="aee28-199">Erstellen des ASF-Profil Objekts</span><span class="sxs-lookup"><span data-stu-id="aee28-199">Create the ASF Profile Object</span></span>

<span data-ttu-id="aee28-200">Damit die ASF-Datei-Senke codierte Mediendaten in eine ASF-Datei schreibt, muss die Senke die Anzahl der Streams und den Typ der Streams kennen, für die streamsenken erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-200">For the ASF file sink to write encoded media data into an ASF file, the sink needs to know the number of streams and the type of streams for which to create stream sinks.</span></span> <span data-ttu-id="aee28-201">In diesem Tutorial extrahieren Sie diese Informationen aus der Medienquelle und erstellen entsprechende Ausgabedaten Ströme.</span><span class="sxs-lookup"><span data-stu-id="aee28-201">In this tutorial you will extract that information from the media source and create corresponding output streams.</span></span> <span data-ttu-id="aee28-202">Beschränken Sie die Ausgabestreams auf einen Audiostream und einen Videostream.</span><span class="sxs-lookup"><span data-stu-id="aee28-202">Restrict your output streams to one audio stream and one video stream.</span></span> <span data-ttu-id="aee28-203">Erstellen Sie für jeden ausgewählten Stream in der Quelle einen Zielstream, und fügen Sie ihn dem Profil hinzu.</span><span class="sxs-lookup"><span data-stu-id="aee28-203">For each selected stream in the source, create a target stream and add it to the profile.</span></span>

<span data-ttu-id="aee28-204">Um diesen Schritt zu implementieren, benötigen Sie die folgenden Objekte.</span><span class="sxs-lookup"><span data-stu-id="aee28-204">To implement this step, you need the following objects.</span></span>

-   [<span data-ttu-id="aee28-205">ASF-Profil</span><span class="sxs-lookup"><span data-stu-id="aee28-205">ASF Profile</span></span>](asf-profile.md)
-   <span data-ttu-id="aee28-206">Präsentations Deskriptor für die Medienquelle</span><span class="sxs-lookup"><span data-stu-id="aee28-206">Presentation Descriptor for the media source</span></span>
-   <span data-ttu-id="aee28-207">Streamdeskriptoren für die ausgewählten Streams in der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="aee28-207">Stream descriptors for the selected streams in the media source.</span></span>
-   <span data-ttu-id="aee28-208">Medientypen für die ausgewählten Streams.</span><span class="sxs-lookup"><span data-stu-id="aee28-208">Media Types for the selected streams.</span></span>

<span data-ttu-id="aee28-209">In den folgenden Schritten wird beschrieben, wie das ASF-Profil und die zielstreams erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-209">The following steps describe the process of creating the ASF profile and the target streams.</span></span>

<span data-ttu-id="aee28-210">**So erstellen Sie das ASF-Profil**</span><span class="sxs-lookup"><span data-stu-id="aee28-210">**To create the ASF profile**</span></span>

1.  <span data-ttu-id="aee28-211">Rufen Sie [**mfkreateasfprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) auf, um ein leeres Profil Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aee28-211">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty profile object.</span></span>
2.  <span data-ttu-id="aee28-212">Rufen Sie [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) auf, um den Präsentations Deskriptor für die Medienquelle zu erstellen, die Sie in diesem Tutorial im Abschnitt "Erstellen der Medienquelle" beschrieben haben.</span><span class="sxs-lookup"><span data-stu-id="aee28-212">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to create the presentation descriptor for the media source created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
3.  <span data-ttu-id="aee28-213">Aufrufen Sie [**imfpresentationdescriptor:: getstreamdescriptorcount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) , um die Anzahl der Streams in der Medienquelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-213">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the media source.</span></span>
4.  <span data-ttu-id="aee28-214">Aufrufen von [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) für jeden Stream in der Medienquelle Ruft den streamdeskriptor des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="aee28-214">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) for each stream in the media source, get the stream's stream descriptor.</span></span>
5.  <span data-ttu-id="aee28-215">Aufrufen von [**imfstreamdescriptor:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) gefolgt von [**imfmediatypeer Handler:: getmediatypeer byindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) und Abrufen des ersten Medientyps für den Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="aee28-215">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) followed by [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) and get the first media type for the stream.</span></span>

    <span data-ttu-id="aee28-216">**Hinweis**   Um komplexe Aufrufe zu vermeiden, gehen Sie davon aus, dass nur ein Medientyp pro Stream vorhanden ist, und wählen Sie den ersten Medientyp des Streams aus.</span><span class="sxs-lookup"><span data-stu-id="aee28-216">**Note**   To avoid complex calls, assume that only one media type exists per stream and select the first media type of the stream.</span></span> <span data-ttu-id="aee28-217">Bei komplexen Streams müssen Sie jeden Medientyp aus dem Medientyp Handler auflisten und den Medientyp auswählen, den Sie codieren möchten.</span><span class="sxs-lookup"><span data-stu-id="aee28-217">For complex streams, you need to enumerate each media type from the media type handler and choose the media type that you would like to encode.</span></span>

6.  <span data-ttu-id="aee28-218">Aufrufen von "I [**imfmediatype:: getmajortype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) " zum Abrufen des Haupttyps des Streams, um zu bestimmen, ob der Stream Audiodaten oder Videos enthält.</span><span class="sxs-lookup"><span data-stu-id="aee28-218">Call I [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) to get the major type of the stream to determine whether the stream is contains audio or video.</span></span>
7.  <span data-ttu-id="aee28-219">Erstellen Sie, abhängig vom Haupttyp des Streams, Zielmedien Typen.</span><span class="sxs-lookup"><span data-stu-id="aee28-219">Depending on the major type of the stream, create target media types.</span></span> <span data-ttu-id="aee28-220">Diese Medientypen enthalten Formatinformationen, die vom Encoder während der Codierungs Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-220">These media types will hold format information that the encoder will use during the encoding session.</span></span> <span data-ttu-id="aee28-221">In den folgenden Abschnitten dieses Lernprogramms wird der Prozess der Erstellung der Zielmedien Typen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aee28-221">The following sections of this tutorial describe the process of creating the target media types.</span></span>
    -   <span data-ttu-id="aee28-222">Erstellen eines komprimierten Audiomedien Typs</span><span class="sxs-lookup"><span data-stu-id="aee28-222">Create a Compressed Audio Media Type</span></span>
    -   <span data-ttu-id="aee28-223">Erstellen eines komprimierten Video Medientyps</span><span class="sxs-lookup"><span data-stu-id="aee28-223">Create a Compressed Video Media Type</span></span>
8.  <span data-ttu-id="aee28-224">Erstellen Sie einen Datenstrom auf der Grundlage des Zielmedien Typs, konfigurieren Sie den Stream gemäß den Anforderungen der Anwendung, und fügen Sie den Stream zum Profil hinzu.</span><span class="sxs-lookup"><span data-stu-id="aee28-224">Create a stream based on the target media type, configure the stream according to the application's requirements, and add the stream to the profile.</span></span> <span data-ttu-id="aee28-225">Weitere Informationen finden Sie unter [Hinzufügen von Datenstrom Informationen zur-Senke der ASF-Datei](adding-stream-information-to-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-225">For more information, see [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

    1.  <span data-ttu-id="aee28-226">Rufen Sie [**imfasfprofile:: foratestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) auf, und übergeben Sie den Zielmedientyp, um den Ausgabedatenstrom zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aee28-226">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) and pass the target media type to create the output stream.</span></span> <span data-ttu-id="aee28-227">Die-Methode ruft die imfassstreamconfig-Schnittstelle des Stream-Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="aee28-227">The method retrieves the IMFASFStreamConfig interface of the stream object.</span></span>
    2.  <span data-ttu-id="aee28-228">Konfigurieren Sie den Stream.</span><span class="sxs-lookup"><span data-stu-id="aee28-228">Configure the stream.</span></span>
        -   <span data-ttu-id="aee28-229">Aufrufen von [**imfasfstreamconfig:: setstreamnumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) , um dem Stream eine Zahl zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="aee28-229">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a number to the stream.</span></span> <span data-ttu-id="aee28-230">Diese Einstellung ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="aee28-230">This setting is mandatory.</span></span>
        -   <span data-ttu-id="aee28-231">Konfigurieren Sie optional die Lecks-Bucket-Parameter, die Nutz Last Erweiterung und den gegenseitigen Ausschluss für jeden Stream, indem Sie [**imfasfstreamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Methoden und relevante Datenstrom-Konfigurations Attribute aufrufen</span><span class="sxs-lookup"><span data-stu-id="aee28-231">Optionally configure the leaky bucket parameters, payload extension, mutual exclusion on each stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods and relevant stream configuration attributes.</span></span>
    3.  <span data-ttu-id="aee28-232">Fügen Sie die Codierungs Eigenschaften auf Streamebene mithilfe des ASF ContentInfo-Objekts hinzu.</span><span class="sxs-lookup"><span data-stu-id="aee28-232">Add the stream level encoding properties by using the ASF ContentInfo object.</span></span> <span data-ttu-id="aee28-233">Weitere Informationen zu diesem Schritt finden Sie im Abschnitt "Erstellen des ASF-ContentInfo-Objekts" in diesem Tutorial.</span><span class="sxs-lookup"><span data-stu-id="aee28-233">For more information about this step, see the "Create the ASF ContentInfo Object" section in this tutorial.</span></span>
    4.  <span data-ttu-id="aee28-234">Aufrufen von [**imfasfprofile:: setStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) , um den Stream zum Profil hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="aee28-234">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the stream to the profile.</span></span>

    <span data-ttu-id="aee28-235">Im folgenden Codebeispiel wird ein ausgabeaudiodatenstrom erstellt.</span><span class="sxs-lookup"><span data-stu-id="aee28-235">The following code example creates an output audio stream.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    <span data-ttu-id="aee28-236">Das folgende Codebeispiel erstellt einen ausgabevideostream.</span><span class="sxs-lookup"><span data-stu-id="aee28-236">The following code example creates an output video stream.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateVideoStream
    //  Create an video stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //    pType: A pointer to the source's video media type.
    //-------------------------------------------------------------------

    HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        HRESULT hr = S_OK;

        
        IMFMediaType* pVideoType = NULL;
        IMFASFStreamConfig* pVideoStream = NULL;

        UINT32 dwBitRate = 0;
            
        //Create a new video type from the source type
        hr = CreateCompressedVideoType(pType, &pVideoType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Create a new stream with the video type
        hr = pProfile->CreateStream(pVideoType, &pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }
        

        //Set a valid stream number
        hr = pVideoStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }

        //Add the stream to the profile
        hr = pProfile->SetStream(pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

    done:

        SafeRelease(&pVideoStream);
        SafeRelease(&pVideoType);

        return hr;
    }
    ```

    

<span data-ttu-id="aee28-237">Im folgenden Codebeispiel werden die Ausgabestreams abhängig von den Datenströmen in der Quelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="aee28-237">The following code example creates output streams depending on the streams in the source.</span></span>


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a><span data-ttu-id="aee28-238">Erstellen eines komprimierten Audiomedien Typs</span><span class="sxs-lookup"><span data-stu-id="aee28-238">Create a Compressed Audio Media Type</span></span>

<span data-ttu-id="aee28-239">Wenn Sie einen Audiostream in die Ausgabedatei einschließen möchten, erstellen Sie einen Audiotyp, indem Sie die Merkmale des codierten Typs angeben, indem Sie die erforderlichen Attribute festlegen.</span><span class="sxs-lookup"><span data-stu-id="aee28-239">If you want to include an audio stream in the output file, create an audio type by specifying the characteristics of the encoded type by setting the required attributes.</span></span> <span data-ttu-id="aee28-240">Um sicherzustellen, dass der Audiotyp mit dem Windows Media-Audioencoder kompatibel ist, instanziieren Sie den Encoder-MFT, legen Sie die Codierungs Eigenschaften fest, und rufen Sie einen Medientyp durch Aufrufen von [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)ab.</span><span class="sxs-lookup"><span data-stu-id="aee28-240">To make sure that the audio type is compatible with the Windows Media audio encoder, instantiate the encoder MFT, set the encoding properties, and get a media type by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="aee28-241">Sie können den erforderlichen Ausgabetyp durchlaufen, indem Sie alle verfügbaren Typen durchlaufen, die Attribute der einzelnen Medientypen erhalten und den Typ auswählen, der Ihren Anforderungen am ehesten entspricht.</span><span class="sxs-lookup"><span data-stu-id="aee28-241">Get the required output type by looping through all the available types, getting the attributes of each media type, and selecting the type that is closest to your requirements.</span></span> <span data-ttu-id="aee28-242">In diesem Tutorial können Sie den ersten verfügbaren Typ aus der Liste der vom Encoder unterstützten Ausgabemedien Typen erhalten.</span><span class="sxs-lookup"><span data-stu-id="aee28-242">In this tutorial, get the first available type from the list of output media types supported by the encoder.</span></span>

<span data-ttu-id="aee28-243">**Hinweis**  Für Windows 7 stellt Media Foundation eine neue Funktion, [**mftranscodegetaudiooutputavailabletypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) , bereit, mit der eine Liste der kompatiblen Audiotypen abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-243">**Note**  For Windows 7, Media Foundation provides a new function, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) that retrieves a list of the compatible audio types.</span></span> <span data-ttu-id="aee28-244">Diese Funktion ruft nur die Medientypen für die CBR-Codierung ab.</span><span class="sxs-lookup"><span data-stu-id="aee28-244">This function only gets media types for CBR encoding.</span></span>

<span data-ttu-id="aee28-245">Für einen kompletten Audiotyp müssen die folgenden Attribute festgelegt sein:</span><span class="sxs-lookup"><span data-stu-id="aee28-245">A complete audio type must have the following attributes set:</span></span>

-   [<span data-ttu-id="aee28-246">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aee28-246">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)
-   [<span data-ttu-id="aee28-247">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="aee28-247">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)
-   [<span data-ttu-id="aee28-248">**MF \_ \_ -MT- \_ audionum- \_ Kanäle**</span><span class="sxs-lookup"><span data-stu-id="aee28-248">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)
-   [<span data-ttu-id="aee28-249">**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="aee28-249">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)
-   [<span data-ttu-id="aee28-250">**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="aee28-250">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="aee28-251">**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="aee28-251">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="aee28-252">**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**</span><span class="sxs-lookup"><span data-stu-id="aee28-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)

<span data-ttu-id="aee28-253">Im folgenden Codebeispiel wird ein komprimierter Audiotyp erstellt, indem ein kompatibler Typ aus dem Windows Media Audio Encoder erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-253">The following code example creates a compressed audio type by getting a compatible type from the Windows Media Audio encoder.</span></span> <span data-ttu-id="aee28-254">Die Implementierung von setencodingproperties wird im Abschnitt "Erstellen des ASF-ContentInfo-Objekts" in diesem Tutorial gezeigt.</span><span class="sxs-lookup"><span data-stu-id="aee28-254">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a><span data-ttu-id="aee28-255">Erstellen eines komprimierten Video Medientyps</span><span class="sxs-lookup"><span data-stu-id="aee28-255">Create a Compressed Video Media Type</span></span>

<span data-ttu-id="aee28-256">Wenn Sie einen Videostream in die Ausgabedatei einschließen möchten, erstellen Sie einen komplett codierten Videotyp.</span><span class="sxs-lookup"><span data-stu-id="aee28-256">If you want to include a video stream in the output file, create a complete-encoded video type.</span></span> <span data-ttu-id="aee28-257">Der gesamte Medientyp muss die gewünschte Bitrate und die privaten Codec-Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="aee28-257">The complete media type must include the desired bit rate and codec private data.</span></span>

<span data-ttu-id="aee28-258">Es gibt zwei Möglichkeiten, einen gesamten Video Medientyp zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aee28-258">There are two ways you can create a complete video media type.</span></span>

-   <span data-ttu-id="aee28-259">Erstellen Sie einen leeren Medientyp, kopieren Sie die Medientyp Attribute aus dem Quell Videotyp, und überschreiben Sie das Attribut " [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) " mit der GUID-Konstante "MF Videoformat \_ WMV3".</span><span class="sxs-lookup"><span data-stu-id="aee28-259">Create an empty media type and copy the media type attributes from the source video type and overwrite the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute with the GUID constant MFVideoFormat\_WMV3.</span></span>

    <span data-ttu-id="aee28-260">Für einen kompletten Videotyp müssen die folgenden Attribute festgelegt sein:</span><span class="sxs-lookup"><span data-stu-id="aee28-260">A complete video type must have the following attributes set:</span></span>

    -   <span data-ttu-id="aee28-261">Haupt-Typ des MF- \_ MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="aee28-261">MF\_MT\_MAJOR\_TYPE</span></span>
    -   <span data-ttu-id="aee28-262">MF- \_ MT- \_ Untertyp</span><span class="sxs-lookup"><span data-stu-id="aee28-262">MF\_MT\_SUBTYPE</span></span>
    -   <span data-ttu-id="aee28-263">MF- \_ MT- \_ Frame \_ Rate</span><span class="sxs-lookup"><span data-stu-id="aee28-263">MF\_MT\_FRAME\_RATE</span></span>
    -   <span data-ttu-id="aee28-264">MF- \_ MT- \_ Frame \_ Größe</span><span class="sxs-lookup"><span data-stu-id="aee28-264">MF\_MT\_FRAME\_SIZE</span></span>
    -   <span data-ttu-id="aee28-265">MF- \_ MT- \_ Interlace- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="aee28-265">MF\_MT\_INTERLACE\_MODE</span></span>
    -   <span data-ttu-id="aee28-266">Verhältnis der MF- \_ MT- \_ Pixel \_ Seite \_</span><span class="sxs-lookup"><span data-stu-id="aee28-266">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>
    -   <span data-ttu-id="aee28-267">MF-mittlere mittlere \_ \_ \_ Bitrate</span><span class="sxs-lookup"><span data-stu-id="aee28-267">MF\_MT\_AVG\_BITRATE</span></span>
    -   <span data-ttu-id="aee28-268">\_ \_ Benutzer \_ Daten für MF-MT</span><span class="sxs-lookup"><span data-stu-id="aee28-268">MF\_MT\_USER\_DATA</span></span>

    <span data-ttu-id="aee28-269">Im folgenden Codebeispiel wird ein komprimierter Videotyp aus dem Videotyp der Quelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="aee28-269">The following code example creates a compressed video type from the source's video type.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   <span data-ttu-id="aee28-270">Abrufen eines kompatiblen Medientyps aus dem Windows Media-Video Encoder durch Festlegen der Codierungs Eigenschaften und anschließendes Aufrufen von [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="aee28-270">Get a compatible media type from the Windows Media video encoder by setting the encoding properties and then calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="aee28-271">Diese Methode gibt den partiellen Typ zurück.</span><span class="sxs-lookup"><span data-stu-id="aee28-271">This method returns the partial type.</span></span> <span data-ttu-id="aee28-272">Stellen Sie sicher, dass Sie den partiellen Typ in einen vollständigen Typ konvertieren, indem Sie folgende Informationen hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="aee28-272">Make sure you convert the partial type to a complete type by adding the following information:</span></span>

    -   <span data-ttu-id="aee28-273">Legen Sie die Video [**Bitrate im MF \_ MT \_ AVG- \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) -Attribut fest.</span><span class="sxs-lookup"><span data-stu-id="aee28-273">Set the video bit rate in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute.</span></span>
    -   <span data-ttu-id="aee28-274">Fügen Sie private Codec-Daten hinzu, indem Sie das [**MF \_ MT- \_ Benutzer \_ Daten**](mf-mt-user-data-attribute.md) Attribut festlegen.</span><span class="sxs-lookup"><span data-stu-id="aee28-274">Add codec private data by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="aee28-275">Ausführliche Anweisungen finden Sie unter "private Codec-Daten" unter [Konfigurieren eines WMV-Encoders](configuring-a-wmv-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-275">For detailed instructions, see "Private Codec Data" in [Configuring a WMV Encoder](configuring-a-wmv-encoder.md).</span></span>

    <span data-ttu-id="aee28-276">Da [**iwmcodecprivatedata:: getprivatedata**](../wmformat/iwmcodecprivatedata-getprivatedata.md) die Bitrate vor der Rückgabe der privaten Codec-Daten überprüft, stellen Sie sicher, dass Sie die Bitrate festlegen, bevor Sie die privaten Codec-Daten erhalten.</span><span class="sxs-lookup"><span data-stu-id="aee28-276">Because [**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) checks the bit rate before returning the codec private data, make sure that you set the bit rate before getting the codec private data.</span></span>

    <span data-ttu-id="aee28-277">Im folgenden Codebeispiel wird ein komprimierter Videotyp erstellt, indem ein kompatibler Typ aus dem Windows Media Video Encoder erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-277">The following code example creates a compressed video type by getting a compatible type from the Windows Media Video encoder.</span></span> <span data-ttu-id="aee28-278">Außerdem wird ein unkomprimierter Videotyp erstellt und als Eingabe des Encoders festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aee28-278">It also creates an uncompressed video type and sets it as the encoder's input.</span></span> <span data-ttu-id="aee28-279">Dies wird in der Hilfsfunktion createuncompressedvideotype implementiert.</span><span class="sxs-lookup"><span data-stu-id="aee28-279">This is implemented in the helper function CreateUncompressedVideoType.</span></span> <span data-ttu-id="aee28-280">Getoutputtypeer fromwmvencoder konvertiert den zurückgegebenen partiellen Typ durch Hinzufügen von privaten Codec-Daten in einen vollständigen Typ.</span><span class="sxs-lookup"><span data-stu-id="aee28-280">GetOutputTypeFromWMVEncoder converts the returned partial type into a complete type by adding codec private data.</span></span> <span data-ttu-id="aee28-281">Die Implementierung von setencodingproperties wird im Abschnitt "Erstellen des ASF-ContentInfo-Objekts" in diesem Tutorial gezeigt.</span><span class="sxs-lookup"><span data-stu-id="aee28-281">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    <span data-ttu-id="aee28-282">Im folgenden Codebeispiel wird ein unkomprimierter Videotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="aee28-282">The following code example creates an uncompressed video type.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    <span data-ttu-id="aee28-283">Im folgenden Codebeispiel werden dem angegebenen Video Medientyp private Codec-Daten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aee28-283">The following code example adds codec private data to the specified video media type.</span></span>

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a><span data-ttu-id="aee28-284">Erstellen des ASF-ContentInfo-Objekts</span><span class="sxs-lookup"><span data-stu-id="aee28-284">Create the ASF ContentInfo Object</span></span>

<span data-ttu-id="aee28-285">Das Objekt "ASF ContentInfo" ist eine Komponente auf wmcontainerebene, die in erster Linie zum Speichern von Informationen über das ASF-Header Objekt dient</span><span class="sxs-lookup"><span data-stu-id="aee28-285">The ASF ContentInfo object is a WMContainer level component that is primarily designed to store ASF Header Object information.</span></span> <span data-ttu-id="aee28-286">Die ASF-Datei-Senke implementiert das ContentInfo-Objekt, um Informationen (in einem Eigenschaften Speicher) zu speichern, die zum Schreiben des ASF-Header Objekts der codierten Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-286">The ASF file sink, implements the ContentInfo object in order to store information (in a property store) that will be used to write the ASF Header Object of the encoded file.</span></span> <span data-ttu-id="aee28-287">Zu diesem Zweck müssen Sie vor dem Starten der Codierungs Sitzung den folgenden Satz von Informationen für das ContentInfo-Objekt erstellen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="aee28-287">To do so, you must create and configure the following set of information on the ContentInfo object before starting the encoding session.</span></span>

1.  <span data-ttu-id="aee28-288">Rufen Sie [**mfkreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) auf, um ein leeres ContentInfo-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aee28-288">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>

    <span data-ttu-id="aee28-289">Im folgenden Codebeispiel wird ein leeres ContentInfo-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="aee28-289">The following code example creates an empty ContentInfo object.</span></span>

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="aee28-290">Aufrufen von [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) zum Abrufen des Eigenschafts Speichers auf Datenstrom Ebene der Datei Senke.</span><span class="sxs-lookup"><span data-stu-id="aee28-290">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's stream-level property store.</span></span> <span data-ttu-id="aee28-291">In diesem Befehl müssen Sie die Datenstrom Nummer übergeben, die Sie beim Erstellen des ASF-Profils für den Stream zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="aee28-291">In this call, you need to pass the stream number that you assigned for the stream while creating the ASF profile.</span></span>
3.  <span data-ttu-id="aee28-292">Legen Sie die [Codierungs Eigenschaften](configuring-the-encoder.md) auf Streamebene im Stream-Eigenschaften Speicher der Datei Senke fest.</span><span class="sxs-lookup"><span data-stu-id="aee28-292">Set the stream-level [Encoding Properties](configuring-the-encoder.md) in the file sink's stream property store.</span></span> <span data-ttu-id="aee28-293">Weitere Informationen finden Sie unter "Stream Encoding Properties" unter [Setting Properties in the file Sink](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-293">For more information, see "Stream Encoding Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

    <span data-ttu-id="aee28-294">Im folgenden Codebeispiel werden die Eigenschaften der Streamebene im Eigenschaften Speicher der Datei Senke festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aee28-294">The following code example sets the stream level properties in the file sink's property store.</span></span>

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    <span data-ttu-id="aee28-295">Im folgenden Codebeispiel wird die Implementierung von setencodingproperties veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="aee28-295">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="aee28-296">Diese Funktion legt Codierungs Eigenschaften auf Streamebene für CBR und VBR fest.</span><span class="sxs-lookup"><span data-stu-id="aee28-296">This function sets stream level encoding properties for CBR and VBR.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  SetEncodingProperties
    //  Create a media source from a URL.
    //
    //  guidMT:  Major type of the stream, audio or video
    //  pProps:  A pointer to the property store in which 
    //           to set the required encoding properties.
    //-------------------------------------------------------------------

    HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
    {
        if (!pProps)
        {
            return E_INVALIDARG;
        }

        if (EncodingMode == NONE)
        {
            return MF_E_NOT_INITIALIZED;
        }
       
        HRESULT hr = S_OK;

        PROPVARIANT var;

        switch (EncodingMode)
        {
            case CBR:
                // Set VBR to false.
                hr = InitPropVariantFromBoolean(FALSE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the video buffer window.
                if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            case VBR:
                //Set VBR to true.
                hr = InitPropVariantFromBoolean(TRUE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Number of encoding passes is 1.

                hr = InitPropVariantFromInt32(1, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the quality level.

                if (guidMT == MFMediaType_Audio)
                {
                    hr = InitPropVariantFromUInt32(98, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                else if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromUInt32(95, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            default:
                hr = E_UNEXPECTED;
                break;
        }    

    done:
        PropVariantClear(&var);
        return hr;
    }
    ```

    

4.  <span data-ttu-id="aee28-297">Aufrufen von [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) zum Abrufen des globalen Eigenschafts Speichers der Datei Senke.</span><span class="sxs-lookup"><span data-stu-id="aee28-297">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's global property store.</span></span> <span data-ttu-id="aee28-298">In diesem Befehl müssen Sie 0 im ersten Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="aee28-298">In this call, you need to pass 0 in the first parameter.</span></span> <span data-ttu-id="aee28-299">Weitere Informationen finden Sie unter "globale dateisenke-Eigenschaften" unter [Festlegen von Eigenschaften in der Datei Senke](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-299">For more information, see "Global File Sink Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
5.  <span data-ttu-id="aee28-300">Legen Sie [**mfpkey \_ asfmediasink \_ autoadjust \_ Bitrate**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) auf Variant \_ true fest, um sicherzustellen, dass die Lecks-Bucket-Werte im ASF Multiplexer ordnungsgemäß angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-300">Set the [**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) to VARIANT\_TRUE to ensure the leaky bucket values in the ASF multiplexer are adjusted properly.</span></span> <span data-ttu-id="aee28-301">Weitere Informationen zu dieser Eigenschaft finden Sie unter "Multiplexer-Initialisierung und undichte Bucket-Einstellungen" unter [Erstellen des Multiplexer-Objekts](creating-the-multiplexer-object.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-301">For information about this property, see "Multiplexer Initialization and Leaky Bucket Settings" in [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

    <span data-ttu-id="aee28-302">Im folgenden Codebeispiel werden die Eigenschaften der Streamebene im Eigenschaften Speicher der Datei Senke festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aee28-302">The following code example sets the stream level properties in the file sink's property store.</span></span>

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > <span data-ttu-id="aee28-303">Es gibt weitere Eigenschaften, die Sie auf der globalen Ebene für die Datei Senke festlegen können.</span><span class="sxs-lookup"><span data-stu-id="aee28-303">There are other properties that you can set at the global level for the file sink.</span></span> <span data-ttu-id="aee28-304">Weitere Informationen finden Sie unter "Konfigurieren des ContentInfo-Objekts mit Encodereinstellungen" unter [Festlegen von Eigenschaften im ContentInfo-Objekt](setting-properties-in-the-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-304">For more information, see "Configuring the ContentInfo Object with Encoder Settings" in [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

     

<span data-ttu-id="aee28-305">Verwenden Sie die konfigurierten ASF-ContentInfo, um ein Aktivierungs Objekt für die ASF-Datei-Senke zu erstellen (im nächsten Abschnitt beschrieben).</span><span class="sxs-lookup"><span data-stu-id="aee28-305">You will use the configured ASF ContentInfo to create an activation object for the ASF file sink (described in the next section).</span></span>

<span data-ttu-id="aee28-306">Wenn Sie eine Out-of-Process-Datei Senke ([**mfkreateasfmediasinkactivation**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)) erstellen, die mit einem Aktivierungs Objekt verwendet wird, können Sie das konfigurierte ContentInfo-Objekt verwenden, um die ASF-Medien Senke zu instanziieren (im nächsten Abschnitt beschrieben).</span><span class="sxs-lookup"><span data-stu-id="aee28-306">If you are creating an out-of-process file sink ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), that is by using an activation object, you can use the configured ContentInfo object to instantiate the ASF media sink (described in the next section).</span></span> <span data-ttu-id="aee28-307">Wenn Sie eine in-Process-Datei Senke ([**mfcreateasfmediasink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)) erstellen, anstatt das leere ContentInfo-Objekt wie in Schritt 1 beschrieben zu erstellen, rufen Sie einen Verweis auf die [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle ab, indem Sie **imfmediasink:: QueryInterface** für die Datei Senke aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-307">If you are creating an in-process file sink ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), instead of creating the empty ContentInfo object as described in step 1, get a reference to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface by calling **IMFMediaSink::QueryInterface** on the file sink.</span></span> <span data-ttu-id="aee28-308">Anschließend müssen Sie das ContentInfo-Objekt konfigurieren, wie in diesem Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aee28-308">You must then configure the ContentInfo object as described in this section.</span></span>

### <a name="create-the-asf-file-sink"></a><span data-ttu-id="aee28-309">Erstellen der ASF-Datei-Senke</span><span class="sxs-lookup"><span data-stu-id="aee28-309">Create the ASF File Sink</span></span>

<span data-ttu-id="aee28-310">In diesem Schritt des Tutorials verwenden Sie die konfigurierte Datei "ASF ContentInfo", die Sie im vorherigen Schritt erstellt haben, um ein Aktivierungs Objekt für die ASF-Datei-Senke zu erstellen, indem Sie die [**mfcreateasfmediasinkaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-310">In this step of the tutorial, you will use the configured ASF ContentInfo, which you created in the previous step, to create an activation object for the ASF file sink by calling the [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) function.</span></span> <span data-ttu-id="aee28-311">Weitere Informationen finden Sie unter [Erstellen der ASF-Datei-Senke](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-311">For more information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="aee28-312">Im folgenden Codebeispiel wird das Aktivierungs Objekt für die dateisenke erstellt.</span><span class="sxs-lookup"><span data-stu-id="aee28-312">The following code example creates the activation object for the file sink.</span></span>


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a><span data-ttu-id="aee28-313">Erstellen der partiellen Codierungs Topologie</span><span class="sxs-lookup"><span data-stu-id="aee28-313">Build the Partial Encoding Topology</span></span>

<span data-ttu-id="aee28-314">Als Nächstes erstellen Sie eine partielle Codierungs Topologie, indem Sie topologieknoten für die Medienquelle, die erforderlichen Windows Media Encoder und die ASF-Datei-Senke erstellen.</span><span class="sxs-lookup"><span data-stu-id="aee28-314">Next, you will build a partial encoding topology by creating topology nodes for the media source, the required Windows Media encoders, and the ASF file sink.</span></span> <span data-ttu-id="aee28-315">Nachdem Sie die topologieknoten hinzugefügt haben, verbinden Sie die Quell-, Transformations-und Senke Knoten.</span><span class="sxs-lookup"><span data-stu-id="aee28-315">After adding the topology nodes, you will connect the source, transform, and the sink nodes.</span></span> <span data-ttu-id="aee28-316">Vor dem Hinzufügen von topologieknoten müssen Sie ein leeres Topologieobjekt erstellen, indem Sie [**mfcreatetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-316">Before adding topology nodes, you must create an empty topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span>

### <a name="create-the-source-topology-node-for-the-media-source"></a><span data-ttu-id="aee28-317">Erstellen des Knotens "Quell Topologie" für die Medienquelle</span><span class="sxs-lookup"><span data-stu-id="aee28-317">Create the Source Topology Node for the Media Source</span></span>

<span data-ttu-id="aee28-318">In diesem Schritt erstellen Sie den quelltopologieknoten für die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="aee28-318">In this step, you will create the source topology node for the media source.</span></span>

<span data-ttu-id="aee28-319">Um diesen Knoten zu erstellen, benötigen Sie die folgenden Verweise:</span><span class="sxs-lookup"><span data-stu-id="aee28-319">To create this node you need the following references:</span></span>

-   <span data-ttu-id="aee28-320">Ein Zeiger auf die Medienquelle, die Sie in dem Schritt erstellt haben, der im Abschnitt "Erstellen der Medienquelle" dieses Tutorials beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-320">A pointer to the media source that you created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
-   <span data-ttu-id="aee28-321">Ein Zeiger auf den Präsentations Deskriptor für die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="aee28-321">A pointer to the presentation descriptor for the media source.</span></span> <span data-ttu-id="aee28-322">Sie können einen Verweis auf die imfpresentationdescriptor-Schnittstelle der Medienquelle abrufen, indem Sie [**imfmediasource:: createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-322">You can get a reference to IMFPresentationDescriptor interface of the media source by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="aee28-323">Ein Zeiger auf den Datenstrom Deskriptor für jeden Stream in der Medienquelle, für den Sie einen Zielstream in dem Schritt erstellt haben, den Sie im Abschnitt "Erstellen des ASF-Profil Objekts" dieses Tutorials beschrieben haben.</span><span class="sxs-lookup"><span data-stu-id="aee28-323">A pointer to the stream descriptor for each stream in the media source for which you have created a target stream in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span>

<span data-ttu-id="aee28-324">Weitere Informationen zum Erstellen von Quellknoten und Codebeispielen finden Sie unter [Erstellen von Quellknoten](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-324">For more information about creating source nodes and code example, see [Creating Source Nodes](creating-source-nodes.md).</span></span>

<span data-ttu-id="aee28-325">Im folgenden Codebeispiel wird eine partielle Topologie erstellt, indem der Quellknoten und die erforderlichen Transformations Knoten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-325">The following code example creates a partial topology by adding the source node and the required transform nodes.</span></span> <span data-ttu-id="aee28-326">Mit diesem Code werden die Hilfsfunktionen "addsourcenode" und "addtransformoutputnodes" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-326">This code calls the helper functions AddSourceNode, and AddTransformOutputNodes.</span></span> <span data-ttu-id="aee28-327">Diese Funktionen sind später in diesem Tutorial enthalten.</span><span class="sxs-lookup"><span data-stu-id="aee28-327">These functions are included later in this tutorial.</span></span>


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



<span data-ttu-id="aee28-328">Im folgenden Codebeispiel wird der Codierungs Topologie erstellt und der Knoten der Quell Topologie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aee28-328">The following code example creates and adds the source topology node to the encoding topology.</span></span> <span data-ttu-id="aee28-329">Sie benötigt Zeiger auf ein zuvor Topologieobjekt, die Medienquelle zum Auflisten der Quelldaten Ströme, den Präsentations Deskriptor der Medienquelle und den Datenstrom Deskriptor der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="aee28-329">It takes pointers to a previously topology object, the media source to enumerate the source streams, the media source's presentation descriptor, and the media source's stream descriptor.</span></span> <span data-ttu-id="aee28-330">Der Aufrufer erhält einen Zeiger auf den Knoten der Quell Topologie.</span><span class="sxs-lookup"><span data-stu-id="aee28-330">The caller receives a pointer to the source topology node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a><span data-ttu-id="aee28-331">Instanziieren Sie die erforderlichen Encoder, und erstellen Sie die Transformations Knoten.</span><span class="sxs-lookup"><span data-stu-id="aee28-331">Instantiate the Required Encoders and Create the Transform Nodes</span></span>

<span data-ttu-id="aee28-332">Die Media Foundation Pipeline fügt nicht automatisch die erforderlichen Windows Media Encoder für die Streams ein, die Sie codieren müssen.</span><span class="sxs-lookup"><span data-stu-id="aee28-332">The Media Foundation pipeline does not automatically insert the required Windows Media encoders for the streams that it must encode.</span></span> <span data-ttu-id="aee28-333">Die Anwendung muss die Encoder manuell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="aee28-333">The application must add the encoders manually.</span></span> <span data-ttu-id="aee28-334">Auflisten Sie zu diesem Zweck die Streams im ASF-Profil, das Sie in dem Schritt im Abschnitt "Erstellen des ASF-Profil Objekts" in diesem Tutorial erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="aee28-334">To do so, enumerate the streams in the ASF profile that you created in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span> <span data-ttu-id="aee28-335">Instanziieren Sie für jeden Stream in der Quelle und den entsprechenden Stream im Profil die erforderlichen Encoder.</span><span class="sxs-lookup"><span data-stu-id="aee28-335">For each stream in the source and the corresponding stream in the profile, instantiate the required encoders.</span></span> <span data-ttu-id="aee28-336">Für diesen Schritt benötigen Sie einen Zeiger auf das Aktivierungs Objekt für die Datei Senke, die Sie im Abschnitt "Erstellen der ASF-Datei-Senke" in diesem Tutorial erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="aee28-336">For this step, you need a pointer to the activation object for the file sink that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>

<span data-ttu-id="aee28-337">Eine Übersicht über das Erstellen von Encodern über Aktivierungs Objekte finden [Sie unter Verwenden der Aktivierungs Objekte eines Encoder](using-an-encoder-s-activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-337">For an overview on creating encoders through activation objects, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="aee28-338">Im folgenden Verfahren werden die Schritte beschrieben, die erforderlich sind, um die erforderlichen Encoder zu instanziieren.</span><span class="sxs-lookup"><span data-stu-id="aee28-338">The following procedure describes the steps required to instantiate the required encoders.</span></span>

1.  <span data-ttu-id="aee28-339">Rufen Sie einen Verweis auf das ContentInfo-Objekt der Senke ab, indem Sie [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) für die Datei Senke aktivieren und dann [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) aus der Datei Senke Abfragen, indem Sie **QueryInterface** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-339">Get a reference to the sink's ContentInfo object by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the file sink activate and then querying for [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) from the file sink by calling **QueryInterface**.</span></span>
2.  <span data-ttu-id="aee28-340">Rufen Sie das mit dem ContentInfo-Objekt verknüpfte ASF-Profil durch Aufrufen von [**imfasfcontentinfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)ab.</span><span class="sxs-lookup"><span data-stu-id="aee28-340">Get the ASF profile associated with the ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>
3.  <span data-ttu-id="aee28-341">Listet die Streams im Profil auf.</span><span class="sxs-lookup"><span data-stu-id="aee28-341">Enumerate the streams in the profile.</span></span> <span data-ttu-id="aee28-342">Hierfür benötigen Sie die Anzahl der Datenströme und einen Verweis auf die [**imfasfstreamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstelle jedes Streams.</span><span class="sxs-lookup"><span data-stu-id="aee28-342">For this you will need the stream count and a reference to each stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

    <span data-ttu-id="aee28-343">Wenden Sie die folgenden Methoden an:</span><span class="sxs-lookup"><span data-stu-id="aee28-343">Call the following methods:</span></span>

    -   [<span data-ttu-id="aee28-344">**Imfasf profile:: getstreamcount**</span><span class="sxs-lookup"><span data-stu-id="aee28-344">**IMFASFProfile::GetStreamCount**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [<span data-ttu-id="aee28-345">**Imfasf profile:: GetStream**</span><span class="sxs-lookup"><span data-stu-id="aee28-345">**IMFASFProfile::GetStream**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  <span data-ttu-id="aee28-346">Für jeden Stream erhalten Sie den Haupttyp und die Codierungs Eigenschaften des Streams aus dem ContentInfo-Objekt.</span><span class="sxs-lookup"><span data-stu-id="aee28-346">For each stream get the major type and the stream's encoding properties from the ContentInfo object.</span></span>

    <span data-ttu-id="aee28-347">Wenden Sie die folgenden Methoden an:</span><span class="sxs-lookup"><span data-stu-id="aee28-347">Call the following methods:</span></span>

    -   [<span data-ttu-id="aee28-348">**Imfasf streamconfig:: getmediatype**</span><span class="sxs-lookup"><span data-stu-id="aee28-348">**IMFASFStreamConfig::GetMediaType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [<span data-ttu-id="aee28-349">**IMF MediaType:: getmajortype**</span><span class="sxs-lookup"><span data-stu-id="aee28-349">**IMFMediaType::GetMajorType**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [<span data-ttu-id="aee28-350">**Imfasbcontentinfo:: getencodingconfigurationpropertystore**</span><span class="sxs-lookup"><span data-stu-id="aee28-350">**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        <span data-ttu-id="aee28-351">Für diesen Befehl benötigen Sie die vom [**imfasfprofile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) -Befehl abgerufene Datenstrom Nummer.</span><span class="sxs-lookup"><span data-stu-id="aee28-351">For this call you need the stream number retrieved by the [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) call.</span></span>

5.  <span data-ttu-id="aee28-352">Instanziieren Sie abhängig vom Typ des Streams, der Audiodatei oder des Videos das Aktivierungs Objekt für den Encoder, indem Sie [**mfcreatewmaencoderactivation**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) oder [**mfcreatewmvencoderactivation**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-352">Depending on the type of the stream, audio or video, instantiate the activation object for the encoder by calling [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) or [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span></span>

    <span data-ttu-id="aee28-353">Um diese Funktionen aufzurufen, benötigen Sie die folgenden Verweise:</span><span class="sxs-lookup"><span data-stu-id="aee28-353">To call these functions, you need the following references:</span></span>

    -   <span data-ttu-id="aee28-354">Ein Zeiger auf den Medientyp des Streams, der von [**imfasfstreamconfig:: getmediatype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) im vorherigen Schritt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="aee28-354">A pointer to the stream's media type retrieved by [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) in the previous step.</span></span>
    -   <span data-ttu-id="aee28-355">Ein Zeiger auf den Codierungs Eigenschafts Speicher des Streams, der von [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="aee28-355">A pointer to the stream's encoding property store retrieved by [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore).</span></span> <span data-ttu-id="aee28-356">Durch Übergeben eines Zeigers an den Eigenschaften Speicher werden die in der Datei-Senke festgelegten Stream-Eigenschaften auf die MFT des Encoders kopiert.</span><span class="sxs-lookup"><span data-stu-id="aee28-356">By passing a pointer to the property store, the stream properties set in the file sink are copied on the encoder MFT.</span></span>

6.  <span data-ttu-id="aee28-357">Aktualisieren Sie den Parameter "Leaky Bucket" für den Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="aee28-357">Update the leaky bucket parameter for the audio stream.</span></span>

    <span data-ttu-id="aee28-358">[**Mfkreatewmaencoderaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) legt den Ausgabetyp für den Windows Media-Audiocodec auf dem zugrunde liegenden Encoder-MFT fest.</span><span class="sxs-lookup"><span data-stu-id="aee28-358">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) sets the output type on the underlying encoder MFT for the Windows Media audio codec.</span></span> <span data-ttu-id="aee28-359">Nachdem der Typ des Ausgabe Mediums festgelegt wurde, ruft der Encoder die durchschnittliche Bitrate aus dem Ausgabe Medientyp ab, berechnet die drehbitrate des Puffer Fensters und legt die Lecks-Bucket-Werte fest, die während der Codierungs Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-359">After the output media type is set, the encoder gets the average bit rate from the output media type, calculates the buffer window rage bit rate, and sets the leaky bucket values that will be used during the encoding session.</span></span> <span data-ttu-id="aee28-360">Sie können diese Werte in der Datei Senke aktualisieren, indem Sie entweder den Encoder Abfragen oder benutzerdefinierte Werte festlegen.</span><span class="sxs-lookup"><span data-stu-id="aee28-360">You can update these values in the file sink by either querying the encoder or setting custom values.</span></span> <span data-ttu-id="aee28-361">Zum Aktualisieren von Werten benötigen Sie den folgenden Satz von Informationen:</span><span class="sxs-lookup"><span data-stu-id="aee28-361">To update values you need the following set of information:</span></span>

    -   <span data-ttu-id="aee28-362">Durchschnittliche Bitrate: ermitteln Sie die durchschnittliche Bitrate aus dem für den Ausgabe Medientyp festgelegten Wert für " [**MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) ", der während der Medientyp Aushandlung ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-362">Average bit rate: Get the average bit rate from the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute set on the output media type that is selected during media type negotiation.</span></span>
    -   <span data-ttu-id="aee28-363">Puffer Fenster: Sie können es durch Aufrufen von [**iwmcodecleakybucket:: getbuffersizebits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md)abrufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-363">Buffer window: you can retrieve it by calling [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span>
    -   <span data-ttu-id="aee28-364">Anfängliche Puffergröße: wird auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aee28-364">Initial buffer size: Set to 0.</span></span>

    <span data-ttu-id="aee28-365">Erstellen Sie ein Array von DWords, und legen Sie den Wert in der Eigenschaft " [**mfpkey \_ asfstreamsink \_ korrigiert \_ leakybucket**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) " der Audiodaten Strom-Senke fest.</span><span class="sxs-lookup"><span data-stu-id="aee28-365">Create an array of DWORDs and set the value in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property of the audio stream sink.</span></span> <span data-ttu-id="aee28-366">Wenn Sie die aktualisierten Werte nicht angeben, werden Sie von der Medien Sitzung entsprechend festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aee28-366">If you do not provide the updated values, the Media Session sets them appropriately.</span></span>

    <span data-ttu-id="aee28-367">Weitere Informationen finden Sie unter unkomplizierter [Bucket-Puffer Modell](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-367">For more information, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="aee28-368">Die in Schritt 5 erstellten Aktivierungs Objekte müssen der Topologie als Knoten für die Transformations Topologie hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-368">The activation objects created in step 5 must be added to the topology as transform topology nodes.</span></span> <span data-ttu-id="aee28-369">Weitere Informationen und ein Codebeispiel finden Sie unter "Erstellen eines Transformations Knotens aus einem Aktivierungs Objekt" unter [Erstellen von Transformations Knoten](creating-transform-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-369">For more information and code example, see "Creating a Transform Node from an Activation Object" in [Creating Transform Nodes](creating-transform-nodes.md).</span></span>

<span data-ttu-id="aee28-370">Im folgenden Codebeispiel wird der erforderliche Encoder aktiviert und hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aee28-370">The following code example creates and adds the required encoder activates.</span></span> <span data-ttu-id="aee28-371">Sie benötigt Zeiger auf ein zuvor erstelltes Topologieobjekt, das Aktivierungs Objekt der Datei Senke und den Medientyp des Quelldaten Stroms.</span><span class="sxs-lookup"><span data-stu-id="aee28-371">It takes pointers to a previously created topology object, the file sink's activation object and the source stream's media type.</span></span> <span data-ttu-id="aee28-372">Außerdem wird addoutputnode aufgerufen (siehe nächstes Codebeispiel), mit dem der Senke-Knoten erstellt und der Codierungs Topologie hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-372">It also calls AddOutputNode (see next code example) that creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="aee28-373">Der Aufrufer erhält einen Zeiger auf den Knoten der Quell Topologie.</span><span class="sxs-lookup"><span data-stu-id="aee28-373">It The caller receives a pointer to the source topology node.</span></span>


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a><span data-ttu-id="aee28-374">Erstellen der Knoten für die Ausgabe Topologie für die Datei Senke</span><span class="sxs-lookup"><span data-stu-id="aee28-374">Create the Output Topology Nodes for the File Sink</span></span>

<span data-ttu-id="aee28-375">In diesem Schritt erstellen Sie den Knoten Ausgabe Topologie für die ASF-Datei-Senke.</span><span class="sxs-lookup"><span data-stu-id="aee28-375">In this step, you will create the output topology node for the ASF file sink.</span></span>

<span data-ttu-id="aee28-376">Um diesen Knoten zu erstellen, benötigen Sie die folgenden Verweise:</span><span class="sxs-lookup"><span data-stu-id="aee28-376">To create this node you need the following references:</span></span>

-   <span data-ttu-id="aee28-377">Ein Zeiger auf das Aktivierungs Objekt, das Sie in dem Schritt erstellt haben, der im Abschnitt "Erstellen der ASF-Datei-Senke" dieses Tutorials beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-377">A pointer to the activation object that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>
-   <span data-ttu-id="aee28-378">Die streamnummern zur Identifizierung der Stream-senken, die der Datei Senke hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-378">The stream numbers to identify the stream sinks added to the file sink.</span></span> <span data-ttu-id="aee28-379">Die streamnummern entsprechen der Datenstrom Kennung, die während der Datenstrom Erstellung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="aee28-379">The stream numbers match the stream's identification that was set during stream creation.</span></span>

<span data-ttu-id="aee28-380">Weitere Informationen zum Erstellen von Ausgabe Knoten und Codebeispielen finden Sie unter "Erstellen eines Ausgabe Knotens aus einem Aktivierungs Objekt" unter [Erstellen von Ausgabe Knoten](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-380">For more information about creating output nodes and code example, see "Creating an Output Node from an Activation Object" in [Creating Output Nodes](creating-output-nodes.md).</span></span>

<span data-ttu-id="aee28-381">Wenn Sie kein Aktivierungs Objekt für die Datei-Senke verwenden, müssen Sie die streamsenken in der ASF-Datei-Senke auflisten und jede streamsenke als Ausgabe Knoten in der Topologie festlegen.</span><span class="sxs-lookup"><span data-stu-id="aee28-381">If you are not using activation object for the file sink, you must enumerate the stream sinks in the ASF file sink and set each stream sink as the output node in the topology.</span></span> <span data-ttu-id="aee28-382">Weitere Informationen zur Stream Sink-Enumeration finden Sie unter "Auflisten von streamsenken" unter [Hinzufügen von streaminformationen zur ASF-Datei-Senke](adding-stream-information-to-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-382">For information about stream sink enumeration, see "Enumerating Stream Sinks" in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

<span data-ttu-id="aee28-383">Im folgenden Codebeispiel wird der Codierungs Knoten erstellt und der Codierungs Topologie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="aee28-383">The following code example creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="aee28-384">Sie benötigt Zeiger auf ein zuvor erstelltes Topologieobjekt, das Aktivierungs Objekt der Datei Senke und die Identifikationsnummer des Streams.</span><span class="sxs-lookup"><span data-stu-id="aee28-384">It takes pointers to a previously created topology object, the file sink's activation object and the stream's identification number.</span></span> <span data-ttu-id="aee28-385">Der Aufrufer erhält einen Zeiger auf den Knoten der Quell Topologie.</span><span class="sxs-lookup"><span data-stu-id="aee28-385">It The caller receives a pointer to the source topology node.</span></span>


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



<span data-ttu-id="aee28-386">Im folgenden Codebeispiel werden die streamsenken für eine angegebene Medien Senke aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="aee28-386">The following code example enumerates the stream sinks for a given media sink.</span></span>


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a><span data-ttu-id="aee28-387">Verbinden der Quell-, Transformations-und Senke Knoten</span><span class="sxs-lookup"><span data-stu-id="aee28-387">Connect the Source, Transform, and Sink Nodes</span></span>

<span data-ttu-id="aee28-388">In diesem Schritt verbinden Sie den Quellknoten mit dem Transformations Knoten, der auf die Codierungen verweist, die Sie in diesem Tutorial im Abschnitt "Instanziieren der erforderlichen Encoder und Erstellen der Transformations Knoten" beschrieben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="aee28-388">In this step, you will connect the source node to the transform node referencing the encoding activates that you created in the step described in the "Instantiate the Required Encoders and Create the Transform Nodes" section of this tutorial.</span></span> <span data-ttu-id="aee28-389">Der Transformations Knoten wird mit dem Ausgabe Knoten verbunden, der das Aktivierungs Objekt für die Datei Senke enthält.</span><span class="sxs-lookup"><span data-stu-id="aee28-389">The transform node will be connected to the output node containing the activation object for the file sink.</span></span>

## <a name="handling-the-encoding-session"></a><span data-ttu-id="aee28-390">Verarbeiten der Codierungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="aee28-390">Handling the Encoding Session</span></span>

<span data-ttu-id="aee28-391">In diesem Schritt führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="aee28-391">In the step, you will perform the following steps:</span></span>

1.  <span data-ttu-id="aee28-392">Rufen Sie [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um eine Codierungs Sitzung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aee28-392">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create an encoding session.</span></span>
2.  <span data-ttu-id="aee28-393">Greifen Sie auf [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) zu, um die Codierungs Topologie für die Sitzung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="aee28-393">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the encoding topology on the session.</span></span> <span data-ttu-id="aee28-394">Wenn der-Befehl abgeschlossen ist, wertet die Medien Sitzung die topologieknoten aus und fügt zusätzliche Transformations Objekte ein, z. b. einen Decoder, der die angegebene komprimierte Quelle in nicht komprimierte Beispiele konvertiert, die als Eingabe an den Encoder übergeben werden</span><span class="sxs-lookup"><span data-stu-id="aee28-394">If the call completes, the Media Session evaluates the topology nodes and inserts additional transform objects such as a decoder that converts the specified compressed source to uncompressed samples to feed as input to the encoder.</span></span>
3.  <span data-ttu-id="aee28-395">Wenden Sie [**imfmediasession:: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) an, um die von der Medien Sitzung ausgelöbenen Ereignisse anzufordern.</span><span class="sxs-lookup"><span data-stu-id="aee28-395">Call [**IMFMediaSession::GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) to request for the events raised by the Media Session.</span></span>

    <span data-ttu-id="aee28-396">In der Ereignisschleife starten und schließen Sie die Codierungs Sitzung abhängig von den Ereignissen, die von der Medien Sitzung ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-396">In the event loop you will start and close the encoding session depending on the events raised by the Media Session.</span></span> <span data-ttu-id="aee28-397">Der [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Befehl führt dazu, dass die Medien Sitzung das Ereignis [mesessiontopologystatus](mesessiontopologystatus.md) mit dem Wert für das MF- \_ topostatusready- \_ Flag aufruft.</span><span class="sxs-lookup"><span data-stu-id="aee28-397">The [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) call results in Media Session raising the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag set.</span></span> <span data-ttu-id="aee28-398">Alle Ereignisse werden asynchron generiert, und eine Anwendung kann diese Ereignisse synchron oder asynchron abrufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-398">All events are generated asynchronously and an application can retrieve these events synchronously or asynchronously.</span></span> <span data-ttu-id="aee28-399">Da es sich bei der Anwendung in diesem Tutorial um eine Konsolenanwendung handelt und blockierende Benutzeroberflächenthreads nicht von Bedeutung sind, werden die Ereignisse aus der Medien Sitzung synchron angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aee28-399">Because the application in this tutorial is a console application and blocking user interface threads is not a concern, we will get the events from Media Session synchronously.</span></span>

    <span data-ttu-id="aee28-400">Um die Ereignisse asynchron zu erhalten, muss Ihre Anwendung die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="aee28-400">To get the events asynchronously, your application must implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="aee28-401">Weitere Informationen und ein Beispiel für die Implementierung dieser Schnittstelle finden Sie unter "behandeln von Sitzungs Ereignissen" unter Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="aee28-401">For more information and an example implementation of this interface, see "Handling Session Events" in [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

<span data-ttu-id="aee28-402">Warten Sie in der Ereignisschleife zum Übertragen von Medien Sitzungs Ereignissen auf das Ereignis [mesessiontopologystatus](mesessiontopologystatus.md) , das ausgelöst wird, wenn die [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) abgeschlossen und die Topologie aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-402">In the event loop for getting Media Session events, wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event that is raised when the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) completes and the topology is resolved.</span></span> <span data-ttu-id="aee28-403">Starten Sie nach dem Abrufen des mesessiontopologystatus-Ereignisses die Codierungs Sitzung, indem Sie [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-403">Upon getting the MESessionTopologyStatus event, start the encoding session by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="aee28-404">Die Medien Sitzung generiert das [meendof Presentation](meendofpresentation.md) -Ereignis, wenn alle Codierungs Vorgänge vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="aee28-404">The Media Session generates the [MEEndOfPresentation](meendofpresentation.md) event when all of the encoding operations are complete.</span></span> <span data-ttu-id="aee28-405">Dieses Ereignis muss für die VBR-Codierung behandelt werden und wird im nächsten Abschnitt "Aktualisieren der Codierungs Eigenschaften für die Datei-Senke für die VBR-Codierung" in diesem Tutorial erläutert.</span><span class="sxs-lookup"><span data-stu-id="aee28-405">This event must be handled for VBR encoding and is discussed in the next section "Update Encoding Properties on the File Sink for VBR Encoding" of this tutorial.</span></span>

<span data-ttu-id="aee28-406">Die Medien Sitzung generiert das ASF-Header Objekt und schließt die Datei ab, wenn die Codierungs Sitzung abgeschlossen ist, und löst dann das Ereignis [mesessionclosed](mesessionclosed.md) aus.</span><span class="sxs-lookup"><span data-stu-id="aee28-406">The Media Session generates the ASF Header Object and finalizes the file when the encoding session completes and then raises the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="aee28-407">Dieses Ereignis muss behandelt werden, indem für die Medien Sitzung ordnungsgemäße Herunterfahr Vorgänge durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-407">This event must be handled by performing proper shutdown operations on the Media Session.</span></span> <span data-ttu-id="aee28-408">Um mit dem Herunterfahren zu beginnen, wenden Sie [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)an.</span><span class="sxs-lookup"><span data-stu-id="aee28-408">To begin the shutdown operations, call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="aee28-409">Nachdem die Codierungs Sitzung geschlossen wurde, können Sie keine andere Topologie für die Codierung auf derselben Medien Sitzungs Instanz festlegen.</span><span class="sxs-lookup"><span data-stu-id="aee28-409">After the encoding session is closed, you cannot set another topology for encoding on the same Media Session instance.</span></span> <span data-ttu-id="aee28-410">Um eine andere Datei zu codieren, muss die aktuelle Medien Sitzung geschlossen und freigegeben werden, und die neue Topologie muss für eine neu erstellte Medien Sitzung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-410">To encode another file, the current Media Session must be closed and released and the new topology must be set on a newly created Media Session.</span></span> <span data-ttu-id="aee28-411">Im folgenden Codebeispiel wird die Medien Sitzung erstellt, die Codierungs Topologie festgelegt und die Ereignisse der Medien Sitzung behandelt.</span><span class="sxs-lookup"><span data-stu-id="aee28-411">The following code example creates the Media Session, sets the encoding topology and handles the Media Session events.</span></span>

<span data-ttu-id="aee28-412">Im folgenden Codebeispiel wird die Medien Sitzung erstellt, die Codierungs Topologie festgelegt und die Codierungs Sitzung gesteuert, indem Ereignisse aus der Medien Sitzung behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-412">The following code example creates the Media Session, sets the encoding topology, and controls the encoding session by handling events from the Media Session.</span></span>


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetType(&meType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetStatus(&hrStatus);
        if (FAILED(hr))
        {
            goto done;
        }
        if (FAILED(hrStatus))
        {
            hr = hrStatus;
            goto done;
        }

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a><span data-ttu-id="aee28-413">Aktualisieren der Codierungs Eigenschaften in der Datei Senke</span><span class="sxs-lookup"><span data-stu-id="aee28-413">Update Encoding Properties in the File Sink</span></span>

<span data-ttu-id="aee28-414">Bestimmte Codierungs Eigenschaften, wie z. b. die Codierungs Bitrate und die exakten Werte für den leckwert, werden erst nach Abschluss der Codierung bekannt, insbesondere bei der VBR-Codierung.</span><span class="sxs-lookup"><span data-stu-id="aee28-414">Certain encoding properties such as the encoding bit rate and the accurate leaky bucket values are not known until the encoding is complete, especially for VBR encoding.</span></span> <span data-ttu-id="aee28-415">Um die korrekten Werte zu erhalten, muss die Anwendung auf das [meendofpresentation](meendofpresentation.md) -Ereignis warten, das angibt, dass die Codierungs Sitzung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="aee28-415">To get the correct values the application must wait for the [MEEndOfPresentation](meendofpresentation.md) event that indicates that the encoding session is complete.</span></span> <span data-ttu-id="aee28-416">Die Leaky-Bucket-Werte müssen in der Senke aktualisiert werden, damit das ASF-Header Objekt die exakten Werte widerspiegeln kann.</span><span class="sxs-lookup"><span data-stu-id="aee28-416">The leaky bucket values must be updated in the sink so that the ASF Header Object can reflect the accurate values.</span></span>

<span data-ttu-id="aee28-417">Im folgenden Verfahren werden die Schritte beschrieben, die zum Durchlaufen der Knoten in der Codierungs Topologie erforderlich sind, um den dateisenke-Knoten zu erhalten und die erforderlichen Eigenschaften für das Leaky</span><span class="sxs-lookup"><span data-stu-id="aee28-417">The following procedure describes the steps required to traverse the nodes in the encoding topology to get the file sink node and set the required leaky bucket properties.</span></span>

<span data-ttu-id="aee28-418">**So aktualisieren Sie die Eigenschaftswerte nach der Codierung in der ASF-Datei-Senke**</span><span class="sxs-lookup"><span data-stu-id="aee28-418">**To update the post encoding property values on the ASF file sink**</span></span>

1.  <span data-ttu-id="aee28-419">Aufrufen von [**imftopology:: getoutputnodecollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) zum Abrufen der Ausgabe Knoten Sammlung aus der Codierungs Topologie.</span><span class="sxs-lookup"><span data-stu-id="aee28-419">Call [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) to get the output node collection from the encoding topology.</span></span>
2.  <span data-ttu-id="aee28-420">Rufen Sie für jeden Knoten einen Zeiger auf die streamsenke im Knoten durch Aufrufen von [**imftopologynode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject)ab.</span><span class="sxs-lookup"><span data-stu-id="aee28-420">For each node, get a pointer to the stream sink in the node by calling [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject).</span></span> <span data-ttu-id="aee28-421">Fragen Sie die [**IMF streamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Schnittstelle auf dem [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger ab, der von **imftopologynode:: GetObject** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="aee28-421">Query for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer returned by **IMFTopologyNode::GetObject**.</span></span>
3.  <span data-ttu-id="aee28-422">Rufen Sie für jede streamsenke den downstreamknoten (Encoder) ab, indem Sie [**imftopologynode:: GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-422">For each stream sink get the downstream node (encoder) by calling [**IMFTopologyNode::GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).</span></span>
4.  <span data-ttu-id="aee28-423">Fragen Sie den Knoten ab, um den [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Zeiger vom encoderknoten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="aee28-423">Query the node to get the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer from the encoder node.</span></span>
5.  <span data-ttu-id="aee28-424">Fragen Sie den Encoder nach dem [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger ab, um den Codierungs Eigenschaften Speicher vom Encoder zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="aee28-424">Query the encoder for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the encoding property store from the encoder.</span></span>
6.  <span data-ttu-id="aee28-425">Fragen Sie die streamsenke für den [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger ab, um den Eigenschaften Speicher der Stream-Senke zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="aee28-425">Query the stream sink for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the stream sink's property store.</span></span>
7.  <span data-ttu-id="aee28-426">Rufen Sie [**IPropertyStore:: GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) auf, um die erforderlichen Eigenschaftswerte aus dem Eigenschaften Speicher des Encoders abzurufen und Sie durch Aufrufen von **IPropertyStore:: SetValue** in den Eigenschaften Speicher der Stream-Senke zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="aee28-426">Call [**IPropertyStore::GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) to get the required property values from the encoder's property store and copy them to the stream sink's property store by calling **IPropertyStore::SetValue**.</span></span>

<span data-ttu-id="aee28-427">In der folgenden Tabelle sind die Eigenschaftswerte nach der Codierung aufgeführt, die für die streamsenke für den Videostream festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="aee28-427">The following table shows the post encoding property values that must be set on the stream sink for the video stream.</span></span>



| <span data-ttu-id="aee28-428">Codierungstyp</span><span class="sxs-lookup"><span data-stu-id="aee28-428">Encoding type</span></span>                                                                                  | <span data-ttu-id="aee28-429">Eigenschaftsname (GetValue)</span><span class="sxs-lookup"><span data-stu-id="aee28-429">Property name (GetValue)</span></span>                                                                        | <span data-ttu-id="aee28-430">Eigenschaftsname (SetValue)</span><span class="sxs-lookup"><span data-stu-id="aee28-430">Property name (SetValue)</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aee28-431">Konstante Bitrate-Codierung</span><span class="sxs-lookup"><span data-stu-id="aee28-431">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                   | <span data-ttu-id="aee28-432">mfpkey \_ bavg</span><span class="sxs-lookup"><span data-stu-id="aee28-432">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="aee28-433">mfpkey \_ Ravg</span><span class="sxs-lookup"><span data-stu-id="aee28-433">MFPKEY\_RAVG</span></span><br/>                                                 | <span data-ttu-id="aee28-434">mfpkey \_ stat \_ bavg</span><span class="sxs-lookup"><span data-stu-id="aee28-434">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="aee28-435">mfpkey \_ stat \_ Ravg</span><span class="sxs-lookup"><span data-stu-id="aee28-435">MFPKEY\_STAT\_RAVG</span></span><br/>                                                             |
| [<span data-ttu-id="aee28-436">Qualitäts basierte Variable Bitrate Codierung</span><span class="sxs-lookup"><span data-stu-id="aee28-436">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="aee28-437">mfpkey \_ bavg</span><span class="sxs-lookup"><span data-stu-id="aee28-437">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="aee28-438">mfpkey \_ Ravg</span><span class="sxs-lookup"><span data-stu-id="aee28-438">MFPKEY\_RAVG</span></span><br/> <span data-ttu-id="aee28-439">mfpkey ( \_ bmax)</span><span class="sxs-lookup"><span data-stu-id="aee28-439">MFPKEY\_BMAX</span></span><br/> <span data-ttu-id="aee28-440">mfpkey- \_ Rmax</span><span class="sxs-lookup"><span data-stu-id="aee28-440">MFPKEY\_RMAX</span></span><br/> | <span data-ttu-id="aee28-441">mfpkey \_ stat \_ bavg</span><span class="sxs-lookup"><span data-stu-id="aee28-441">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="aee28-442">mfpkey \_ stat \_ Ravg</span><span class="sxs-lookup"><span data-stu-id="aee28-442">MFPKEY\_STAT\_RAVG</span></span><br/> <span data-ttu-id="aee28-443">mfpkey \_ stat ( \_ bmax)</span><span class="sxs-lookup"><span data-stu-id="aee28-443">MFPKEY\_STAT\_BMAX</span></span><br/> <span data-ttu-id="aee28-444">mfpkey \_ stat \_ Rmax</span><span class="sxs-lookup"><span data-stu-id="aee28-444">MFPKEY\_STAT\_RMAX</span></span><br/> |



 

<span data-ttu-id="aee28-445">Im folgenden Codebeispiel werden die Eigenschaftswerte nach der Codierung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aee28-445">The following code example sets the post-encoding property values.</span></span>


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a><span data-ttu-id="aee28-446">Implementieren von Main</span><span class="sxs-lookup"><span data-stu-id="aee28-446">Implement Main</span></span>

<span data-ttu-id="aee28-447">Das folgende Codebeispiel zeigt die Hauptfunktion der Konsolenanwendung.</span><span class="sxs-lookup"><span data-stu-id="aee28-447">The following code example shows the main function of your console application.</span></span>


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a><span data-ttu-id="aee28-448">Testen der Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="aee28-448">Test the Output File</span></span>

<span data-ttu-id="aee28-449">In der folgenden Liste wird eine Checkliste zum Testen der codierten Datei beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aee28-449">The following list describes a check list for testing the encoded file.</span></span> <span data-ttu-id="aee28-450">Diese Werte können im Dialogfeld Dateieigenschaften aktiviert werden, das Sie anzeigen können, indem Sie mit der rechten Maustaste auf die codierte Datei klicken und im Kontextmenü **Eigenschaften** auswählen.</span><span class="sxs-lookup"><span data-stu-id="aee28-450">These values can be checked in the file properties dialog box that you can display by right-clicking the encoded file and selecting **Properties** from the context menu.</span></span>

-   <span data-ttu-id="aee28-451">Der Pfad der codierten Datei ist richtig.</span><span class="sxs-lookup"><span data-stu-id="aee28-451">The path of the encoded file is accurate.</span></span>
-   <span data-ttu-id="aee28-452">Die Größe der Datei beträgt mehr als 0 KB, und die Wiedergabedauer entspricht der Dauer der Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="aee28-452">The size of the file is more than zero KB and the play duration matches the source file's duration.</span></span>
-   <span data-ttu-id="aee28-453">Überprüfen Sie für den Videostream die Rahmenbreite und-Höhe sowie die Framerate.</span><span class="sxs-lookup"><span data-stu-id="aee28-453">For the video stream, check the frame width and height, frame rate.</span></span> <span data-ttu-id="aee28-454">Diese Werte sollten den Werten entsprechen, die Sie im ASF-Profil angegeben haben, das Sie in dem im Abschnitt "Erstellen des ASF-Profil Objekts" beschriebenen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="aee28-454">These values should match the values that you specified in the ASF profile that you created in the step described in the section "Create the ASF Profile Object".</span></span>
-   <span data-ttu-id="aee28-455">Für den Audiodatenstrom muss die Bitrate nahe dem Wert liegen, den Sie für den Ziel Medientyp angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="aee28-455">For the audio stream, the bit rate must be close to the value you specified on the target media type.</span></span>
-   <span data-ttu-id="aee28-456">Öffnen Sie die Datei in Windows Media Player, und überprüfen Sie die Qualität der Codierung.</span><span class="sxs-lookup"><span data-stu-id="aee28-456">Open the file in Windows Media Player and check the quality of the encoding.</span></span>
-   <span data-ttu-id="aee28-457">Öffnen Sie die ASF-Datei in asfviewer, um die Struktur einer ASF-Datei anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aee28-457">Open the ASF file in ASFViewer to see the structure of an ASF file.</span></span> <span data-ttu-id="aee28-458">Dieses Tool kann von dieser Microsoft- [Website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-458">This tool can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="common-error-codes-and-debugging-tips"></a><span data-ttu-id="aee28-459">Allgemeine Fehler Codes und Tipps zum Debuggen</span><span class="sxs-lookup"><span data-stu-id="aee28-459">Common Error Codes and Debugging Tips</span></span>

<span data-ttu-id="aee28-460">In der folgenden Liste werden die allgemeinen Fehlercodes beschrieben, die möglicherweise von Ihrem empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-460">The following list describes the common error codes that your might receive and the debugging tips.</span></span>

-   <span data-ttu-id="aee28-461">Beim Aufrufen von [**imfsourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) wird die Anwendung angehalten.</span><span class="sxs-lookup"><span data-stu-id="aee28-461">The call to [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) stalls the application.</span></span>

    <span data-ttu-id="aee28-462">Stellen Sie sicher, dass Sie die Media Foundation-Plattform initialisiert haben, indem Sie [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aee28-462">Make sure that you have initialized the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="aee28-463">Diese Funktion richtet die asynchrone Plattform ein, die von allen Methoden verwendet wird, die asynchrone Vorgänge starten, wie z. b. [**IMF sourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), intern.</span><span class="sxs-lookup"><span data-stu-id="aee28-463">This function sets up the asynchronous platform that is used by all methods that start asynchronous operations, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), internally.</span></span>

-   <span data-ttu-id="aee28-464">[**IMF sourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) gibt HRESULT 0x80070002 zurück. "das System kann die angegebene Datei nicht finden.</span><span class="sxs-lookup"><span data-stu-id="aee28-464">[**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) returns HRESULT 0x80070002 "The system cannot find the file specified.</span></span>

    <span data-ttu-id="aee28-465">Stellen Sie sicher, dass der vom Benutzer im ersten Argument angegebene Eingabe Dateiname vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="aee28-465">Make sure that the input file name specified by the user in the first argument exists.</span></span>

-   <span data-ttu-id="aee28-466">HRESULT 0x80070020 "der Prozess kann nicht auf die Datei zugreifen, da Sie von einem anderen Prozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-466">HRESULT 0x80070020 "The process cannot access the file because it is being used by another process.</span></span> <span data-ttu-id="aee28-467">"</span><span class="sxs-lookup"><span data-stu-id="aee28-467">"</span></span>

    <span data-ttu-id="aee28-468">Stellen Sie sicher, dass die Eingabe-und Ausgabedateien zurzeit nicht von einer anderen Ressource im System verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aee28-468">Make sure that the input and the output files are not currently in use by another resource in the system.</span></span>

-   <span data-ttu-id="aee28-469">Aufrufe von [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Methoden geben MF \_ E \_ invalidmediatype zurück.</span><span class="sxs-lookup"><span data-stu-id="aee28-469">Calls to [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods return MF\_E\_INVALIDMEDIATYPE.</span></span>

    <span data-ttu-id="aee28-470">Stellen Sie sicher, dass die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="aee28-470">Make sure that the following conditions are true:</span></span>

    -   <span data-ttu-id="aee28-471">Der Eingabetyp oder der Ausgabetyp, den Sie angegeben haben, ist mit den vom Encoder unterstützten Medientypen kompatibel.</span><span class="sxs-lookup"><span data-stu-id="aee28-471">The input type or the output type that you specified is compatible with media types that the encoder supports.</span></span>
    -   <span data-ttu-id="aee28-472">Die von Ihnen angegebenen Medientypen sind fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="aee28-472">The media types that you specified are complete.</span></span> <span data-ttu-id="aee28-473">Weitere Informationen zu den Medientypen finden Sie im Abschnitt "Erstellen eines komprimierten audiomediums" und "Erstellen eines komprimierten Video Medientyps" in diesem Tutorial.</span><span class="sxs-lookup"><span data-stu-id="aee28-473">For media types to be complete, see the required attributes in the "Create a Compressed Audio Media Type" and "Create a Compressed Video Media Type" sections of this tutorial.</span></span>
    -   <span data-ttu-id="aee28-474">Stellen Sie sicher, dass Sie die Zielbitrate für den partiellen Medientyp festgelegt haben, dem Sie die privaten Codec-Daten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="aee28-474">Make sure that you have set the target bit rate on the partial media type to which you are adding the codec private data.</span></span>

-   <span data-ttu-id="aee28-475">Die Medien Sitzung gibt den \_ \_ nicht unterstützten D3D-Typ von MF E \_ \_ im Ereignis Status zurück.</span><span class="sxs-lookup"><span data-stu-id="aee28-475">The Media Session returns MF\_E\_UNSUPPORTED\_D3D\_TYPE in the event status.</span></span>

    <span data-ttu-id="aee28-476">Dieser Fehler wird zurückgegeben, wenn der Medientyp der Quelle einen gemischten damit-Modus angibt, der nicht von Windows Media Video Encoder unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="aee28-476">This error is returned when the source's media type indicates a mixed interlace mode that is not supported by Windows Media Video encoder.</span></span> <span data-ttu-id="aee28-477">Wenn Ihr komprimierter Video Medientyp für die Verwendung von progressivem Modus festgelegt ist, muss die Pipeline eine Deinterlacing-Transformation verwenden.</span><span class="sxs-lookup"><span data-stu-id="aee28-477">If your compressed video media type is set to use progressive mode, the pipeline must use a de-interlacing transform.</span></span> <span data-ttu-id="aee28-478">Da die Pipeline keine Abgleich findet (Dies wird durch diesen Fehlercode angezeigt), müssen Sie manuell einen Deinterlacer (transcode-Videoprozessor) zwischen dem Decoder und den encoderknoten einfügen.</span><span class="sxs-lookup"><span data-stu-id="aee28-478">Because the pipeline is unable to find a match (indicated by this error code), you must insert a de-interlacer (transcode video processor) between the decoder and encoder nodes manually.</span></span>

-   <span data-ttu-id="aee28-479">Die Medien Sitzung gibt E \_ invalidArg im Ereignis Status zurück.</span><span class="sxs-lookup"><span data-stu-id="aee28-479">The Media Session returns E\_INVALIDARG in the event status.</span></span>

    <span data-ttu-id="aee28-480">Dieser Fehler wird zurückgegeben, wenn die Medientyp Attribute der Quelle nicht mit den Attributen des auf dem Windows Media Encoder festgelegten Ausgabemedien Typs kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="aee28-480">This error is returned when the source's media type attributes are not compatible with the attributes of the output media type set on the Windows Media encoder.</span></span>

-   <span data-ttu-id="aee28-481">[**Iwmcodecprivatedata:: getprivatedata**](../wmformat/iwmcodecprivatedata-getprivatedata.md) gibt HRESULT 0x80040203 "ein Syntax Fehler bei dem Versuch, eine Abfrage Zeichenfolge auszuwerten" zurück.</span><span class="sxs-lookup"><span data-stu-id="aee28-481">[**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) returns HRESULT 0x80040203 "A syntax error occurred trying to evaluate a query string"</span></span>

    <span data-ttu-id="aee28-482">Stellen Sie sicher, dass der Eingabetyp für den Encoder-MFT festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aee28-482">Make sure that the input type is set on the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aee28-483">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aee28-483">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aee28-484">Komponenten der Pipeline Schicht-ASF</span><span class="sxs-lookup"><span data-stu-id="aee28-484">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
