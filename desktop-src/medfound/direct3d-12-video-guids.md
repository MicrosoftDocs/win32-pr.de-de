---
description: Die folgenden GUIDs unterstützen Direct3D 12-Video-APIs.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: Direct3D 12 Video-GUIDs (D3d11. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05f7a56227ccc2953504d8466a34d6b2160ce1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214316"
---
# <a name="direct3d-12-video-guids"></a>Direct3D 12 Video-GUIDs

Die folgenden GUIDs unterstützen Direct3D 12-Video-APIs.

## <a name="d3d12_video_decode_profile-guids"></a>D3D12 \\ _VIDEO \\ _DECODE \\ _PROFILE GUIDs

In der folgenden Tabelle werden die GUIDs aufgelistet, die Direct3D 12-videodecodierprofile identifizieren. In den Beschreibungen wird jedes Direct3D 12-Video-decodieren-Profil mit dem entsprechenden Direct3D 11-Video oder DXVA-Profil verknüpft.

| Name                                                 | Wert                                                                                | BESCHREIBUNG
|------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| D3D12 \_ \_ -Video-decodieren des \_ Profils \_ MPEG1 \_ und \_ MPEG2           | 0x86695f 12, 0x340e, 0x4F, 0x9F, 0xd3, 0x92, 0x53, 0xDD, 0x32, 0x74, 0x60 | Entspricht DXVA2 \_ ModeMPEG2and1 \_ VLD.                 |
| D3D12- \_ Video- \_ Decodieren von \_ Profilen \_                     | 0xee27417f, 0x5e28, 0x4e65, 0xBE, 0xEA, 0x1D, 0x26, 0xb5, 0x08, 0xAD, 0xC9           | Äquivalent zu D3D11 \_ Decoder \_ profile \_ MPEG2 \_ VLD und DXVA2 \_ ModeMPEG2 \_ VLD.                 |
| D3D12- \_ Video- \_ decodieren- \_ Profil \_ H264                      | 0x1b81be68, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xC0, 0x4F, 0x2E, 0x73, 0xC5       | Äquivalent zu D3D11 \_ Decoder \_ profile \_ H264 \_ VLD \_ nofgt und DXVA \_ ModeH264 \_ VLD \_ nofgt. |
| D3D12- \_ Video- \_ decodieren- \_ Profil \_ H264 \_ Stereo \_ progressiv   | 0xd79be8da, 0x0cf1, 0x4c81, 0xb8, 0x2A, 0x69, 0xa4, 0xe2, 0x36, 0xf4, 0x3D          | Äquivalent zu D3D11 \_ Decoder \_ profile \_ H264 \_ VLD \_ Stereo \_ progressiv \_ und DXVA \_ ModeH264 \_ VLD \_ Stereo \_ Progressive \_ nofgt. |
| D3D12- \_ Video- \_ decodieren- \_ Profil \_ H264 \_ Stereo               | 0xf9aaccbb, 0xc2b6, 0x4cfc, 0x87, 0x79, 0x57, 0x07, 0xb1, 0x76, 0x05, 0x52          | Äquivalent zu D3D11 \_ Decoder \_ profile \_ H264 \_ VLD \_ Stereo \_ nofgt and DXVA \_ ModeH264 \_ VLD \_ Stereo \_ nofgt |
| D3D12- \_ Video- \_ decodieren- \_ Profil \_ H264 \_ MultiView            | 0x705b9d82, 0x76cf, 0x49d6, 0xb7, 0xe6, 0xac, 0x88, 0x72, 0xdb, 0x01, 0x3C          | Äquivalent zu D3D11 \_ Decoder \_ profile \_ H264 \_ VLD \_ MultiView \_ nofgt und DXVA \_ ModeH264 \_ VLD \_ MultiView \_ nofgt. |
| D3D12- \_ Video- \_ decodieren- \_ Profil \_ VC1                       | 0x1b81bea3, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xC0, 0x4F, 0x2E, 0x73, 0xC5          | Äquivalent zu D3D11 \_ Decoder \_ profile \_ VC1 \_ VLD und DXVA \_ ModeVC1 \_ VLD. |
| D3D12- \_ Video- \_ decodieren- \_ Profil \_ VC1 \_ D2010                 | 0x1b81bea4, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xC0, 0x4F, 0x2E, 0x73, 0xC5          | Äquivalent zu D3D11 \_ Decoder \_ profile \_ VC1 \_ D2010 und DXVA \_ ModeVC1 \_ D2010. |
| D3D12- \_ Video- \_ decodieren- \_ Profil \_ MPEG4PT2 \_ einfach           | 0xefd64d74, 0xc9e8, 0x41d7, 0xA5, 0xE9, 0xE9, 0xb0, 0xe3, 0x9F, 0xa3, 0x19          | Äquivalent zu D3D11 \_ Decoder \_ profile \_ MPEG4PT2 \_ VLD \_ Simple und DXVA \_ ModeMPEG4pt2 \_ VLD \_ Simple. |
| D3D12- \_ Video- \_ decodieren- \_ Profil \_ MPEG4PT2 \_ advsimple \_ nogmc  | 0xed418a9f, 0x010d, 0x4eda, 0x9a, 0xe3, 0x9a, 0x65, 0x35, 0x8d, 0x8d, 0x2E          | Äquivalent zu D3D11 \_ Decoder \_ profile \_ MPEG4PT2 \_ VLD \_ advsimple \_ nogmc und DXVA \_ ModeMPEG4pt2 \_ VLD \_ advsimple \_ nogmc. |
| D3D12- \_ Video- \_ Decodieren des \_ Profils \_ hevc \_ Main                 | 0x5b11d51b, 0x2F 4C, 0x4452, 0xBC, 0xc3, 0x09, 0xF 2, 0xA1, 0x16, 0x0C, 0xc0          | Äquivalent zu D3D11 \_ Decoder \_ profile \_ hevc \_ VLD \_ Main und DXVA \_ modehevc \_ VLD \_ Main
| D3D12- \_ Video- \_ Decodieren von \_ Profilen \_ hevc \_ MAIN10               | 0x107 af0e0, 0xef1a, 0x4d19, 0xAB, 0xa8, 0x67, 0xA1, 0X63, 0x07, 0x3D, 0x13          | Äquivalent zu D3D11 \_ Decoder \_ profile \_ hevc \_ VLD \_ MAIN10 und DXVA \_ modehevc \_ VLD \_ MAIN10.
| D3D12- \_ Video- \_ decodieren- \_ Profil \_ VP9                       | 0x463707f, 0xa1d0, 0x4585, 0x87, 0x6d, 0x83, 0xAA, 0x6d, 0x60, 0xb8, 0x9E | |
| D3D12- \_ Video- \_ decodieren- \_ Profil \_ VP9 \_ 10bit \_ PROFILE2        | 0xa4c749ef, 0x6ecf, 0x48aa, 0x84, 0x48, 0x50, 0xA7, 0xA1, 0x16, 0x5F, 0xF           | |
| D3D12- \_ Video- \_ decodieren- \_ Profil \_ VP8                       | 0x90b899ea, 0x3a62, 0x4705, 0x88, 0xB3, 0x8d, 0xF 0, 0x4B, 0x27, 0x44, 0xE7 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE0                       | 0xb8be4ccb, 0xcf53, 0x46ba, 0x8d, 0x59, 0xd6, 0xb8, 0xA6, 0xda, 0x5d, 0x2A | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE1                       | 0x6936ff0f, 0x45b1, 0x4163, 0x9C, 0xC1, 0x64, 0x6e, 0xF6, 0x94, 0x61, 0x08 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE2                       | 0x0c5f 2aa1, 0xe541, 0x4089, 0xBB, 0x7b, 0x98, 0x11, 0x0A, 0x19, 0xd7, 0xc8 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_12BIT_PROFILE2                 | 0x17127009, 0xa00f, 0x4ce1, 0x99, 0x4e, 0xBF, 0x40, 0x81, 0xF 6, 0xF 3, 0xF 0 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_12BIT_PROFILE2_420             | 0x2d80bed6, 0x9cac, 0x4835, 0x9E, 0x91, 0x32, 0x7b, 0xBC, 0x4F, 0x9E, 0xe8 | |

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>D3d11. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 11-Video-APIs](direct3d-11-video-apis.md)
</dt> </dl>

 

 




