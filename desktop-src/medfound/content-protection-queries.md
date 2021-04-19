---
description: 'Listet die Abfragen für die IDirect3DAuthenticatedChannel9:: Query-Methode auf.'
ms.assetid: 75e246c6-bf23-44d9-8fb3-46a6dc5324a5
title: Content Protection Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a72f7f054783a644cb352727f4bf65864bf5f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346882"
---
# <a name="content-protection-queries"></a>Content Protection Abfragen

Listet die Abfragen für die [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) -Methode auf.



| Status Anforderung                                                                                                                            | BESCHREIBUNG                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DAUTHENTICATEDQUERY \_ accessibilityattribute**](d3dauthenticatedquery-accessibilityattributes.md)                                   | Gibt den Typ des e/a-Busses zurück, der zum Senden von Daten an die GPU verwendet wurde.                                                                                                   |
| [**D3DAUTHENTICATEDQUERY \_ channelType**](d3dauthenticatedquery-channeltype.md)                                                           | Gibt den Typ des authentifizierten Kanals zurück.                                                                                                                  |
| [**D3DAUTHENTICATEDQUERY \_ CryptoSession**](d3dauthenticatedquery-cryptosession.md)                                                       | Gibt Handles an die Kryptografiesitzung und das Direct3D-Gerät zurück, die einem angegebenen DirectX Video Acceleration 2 (DXVA-2)-Decodergerät zugeordnet sind. |
| [**D3DAUTHENTICATEDQUERY \_ currentverschlüsseltion. barrierefreie**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)                   | Gibt den Verschlüsselungstyp zurück, der angewendet wird, bevor der CPU-oder busbus auf den Inhalt zugreifen kann.                                                            |
| [**D3DAUTHENTICATEDQUERY-Geräte \_ Umgebung**](d3dauthenticatedquery-devicehandle.md)                                                         | Gibt ein Handle für das Gerät zurück, das diesem authentifizierten Kanal zugeordnet ist.                                                                          |
| [**D3DAUTHENTICATEDQUERY \_ Verschlüsselung-accessibleguid**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)                         | Gibt einen der Verschlüsselungstypen zurück, die zum Verschlüsseln von Inhalten verwendet werden können, bevor die CPU oder der Bus darauf zugreifen können.                                     |
| [**D3DAUTHENTICATEDQUERY \_ verschlüsselungszuaccessibleguidcount**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)               | Gibt die Anzahl der Verschlüsselungstypen zurück, die zum Verschlüsseln von Inhalten verwendet werden können, bevor die CPU oder der Bus darauf zugreifen können.                                  |
| [**D3DAUTHENTICATEDQUERY \_ OutputID**](d3dauthenticatedquery-outputid.md)                                                                 | Gibt einen der Ausgabe Bezeichner zurück, der einer angegebenen Kryptografiesitzung und einem Direct3D-Gerät zugeordnet ist.                                        |
| [**D3DAUTHENTICATEDQUERY \_ outputidcount**](d3dauthenticatedquery-outputidcount.md)                                                       | Gibt die Anzahl von Ausgabe Bezeichner zurück, die einer angegebenen Kryptografiesitzung und einem Direct3D-Gerät zugeordnet sind.                                             |
| [**D3DAUTHENTICATEDQUERY \_ Schutz**](d3dauthenticatedquery-protection.md)                                                             | Gibt die aktuelle Schutz Ebene für das Gerät zurück.                                                                                                        |
| [**D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)                   | Gibt Informationen zu einem Prozess zurück, der freigegebene Ressourcen mit eingeschränktem Zugriff öffnen darf.                                                        |
| [**D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocesscount**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)         | Gibt die Anzahl der Prozesse zurück, die zum Öffnen von freigegebenen Ressourcen mit eingeschränktem Zugriff zulässig sind.                                                           |
| [**D3DAUTHENTICATEDQUERY \_ unrestrictedprotectedsharedresourcecount**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) | Gibt die Anzahl der geschützten freigegebenen Ressourcen zurück, die von einem beliebigen Prozess ohne Einschränkungen geöffnet werden können.                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Video-APIs](direct3d-video-apis.md)
</dt> <dt>

[GPU-basiertes Content Protection](gpu-based-content-protection.md)
</dt> </dl>

 

 



