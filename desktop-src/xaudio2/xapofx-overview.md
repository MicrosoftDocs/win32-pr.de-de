---
description: XAPOFX ist eine Sammlung von Audioeffekten, die die XAPO-Schnittstellen für die Verwendung in XAudio2 implementieren. XAPOFX enthält mehrere Effekte und einen gängigen Mechanismus zum Erstellen von Effektinstanzen.
ms.assetid: 762062de-4e19-5e42-8059-e2f8741bd362
title: Übersicht über XAPOFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ae339a022ae5e2e880dcd130dbe055d0fde9cd28a95ea52c1238e2ade080ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005720"
---
# <a name="xapofx-overview"></a>Übersicht über XAPOFX

XAPOFX ist eine Sammlung von Audioeffekten, die [die XAPO-Schnittstellen](xapo-overview.md) für die Verwendung in XAudio2 implementieren. XAPOFX enthält mehrere Effekte und einen gängigen Mechanismus zum Erstellen von Effektinstanzen.

## <a name="included-effects"></a>Eingeschlossene Effekte

In der folgenden Tabelle werden die in XAPOFX enthaltenen Auswirkungen beschrieben. 

| Auswirkung             | Beschreibung                                                                                                                                                                                           | Parameterstruktur                                                     | Parameterkonst constants                                              | Anforderungen                                                                                                              |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| FXECHO             | Ein Echoeffekt.                                                                                                                                                                                       | [**FXECHO-PARAMETER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                         | [**FXECHO-Konstanten**](fxecho-constants.md)                     | Unterstützt nur FLOAT32-Audioformate.                                                                                      |
| FXEQ               | Ein Vier-Band-Equalizer.                                                                                                                                                                                | [**FXEQ-PARAMETER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                             | [**FXEQ-Konstanten**](fxeq-constants.md)                         | Unterstützt nur FLOAT32-Audioformate. Die Abtastrate muss zwischen 22.000 Hz und 48.000 Hz liegen.                             |
| FXMasteringLimiter | Ein Volumelimiter.                                                                                                                                                                                     | [**FXMASTERINGLIMITER-PARAMETER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters) | [**FXMASTERINGLIMIT-Konstanten**](fxmasteringlimit-constants.md) | Unterstützt nur FLOAT32-Audioformate.                                                                                      |
| FXReverb           | Ein einfacher Halleffekt.<br/> XAudio2 bietet auch einen Effekt, derTon Digital Reverb implementieren kann, der mit [**XAudio2CreateReverb instanziiert werden kann.**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)<br/> | [**FXREVERB-PARAMETER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                     | [**FXREVERB-Konstanten**](fxreverb-constants.md)                 | Unterstützt nur FLOAT32-Audioformate. Darüber hinaus unterstützt es nur mono input to mono output (Monoeingabe in mono-Ausgabe) und Stereoeingabe in Stereoausgabe. |



 

## <a name="creating-an-instance-of-an-effect-included-in-xapofx"></a>Erstellen einer Instanz eines in XAPOFX enthaltenen Effekts

XAPOFX bietet die [**CreateFX-Funktion**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) als allgemeinen Mechanismus zum Erstellen von Effektinstanzen. **CreateFX** verwendet die CLSID eines Effekts und gibt einen IUnknown-Schnittstellenzeiger auf eine Instanz des Effekts zurück.

## <a name="using-xapofx-in-xaudio2"></a>Verwenden von XAPOFX in XAudio2

Mit [**CreateFX instanziierte Effekte**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) werden in XAudio2 verwendet, indem sie an Stimmen angefügt werden. Jede XAudio2-Stimme verfügt über eine Effektkette, die null oder mehr Audioeffekte enthält. Audiodaten, die an eine Stimme gesendet werden, werden durch jeden Effekt in der Kette übergeben, bevor sie an die Ausgabeziele der Stimme gesendet werden. Die Stimme übernimmt die Ausgabe jedes Effekts und gibt sie in den nächsten Effekt in der Kette ein, bis keine Auswirkungen in der Kette übrig sind. Um einen XAPOFX-Effekt an eine XAudio2-Stimme anfügen zu können, füllen Sie eine [**XAUDIO2 \_ EFFECT \_ CHAIN-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) mit den Informationen des Effekts aus, und übergeben Sie sie [**an IXAudio2Voice::SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain).

Weitere Informationen zu XAudio2-Effektketten finden Sie unter [XAudio2 Audio Effects](xaudio2-audio-effects.md).

Ein Beispiel für die Verwendung von XAPOFX in XAudio2 finden Sie unter [How to: Use XAPOFX in XAudio2 (Verwenden von XAPOFX in XAudio2).](how-to--use-xapofx-in-xaudio2.md)

## <a name="xaudio2-implicit-effects"></a>Implizite XAudio2-Effekte

Zusätzlich zur Bibliothek von XAPOs, die von XAPOFX bereitgestellt wird, verfügt XAudio2 über integrierte Audioeffekte für Hall und Lautstärkemessung. Sie können diese integrierten Effekte mit [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) und [**XAudio2CreateVolumeMeter erstellen.**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) Unter How to: Create an Effect Chain (How [to: Erstellen einer Effektkette)](how-to--create-an-effect-chain.md) finden Sie ein Beispiel für die Verwendung einer dieser integrierten Effekte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> </dl>

 

 
