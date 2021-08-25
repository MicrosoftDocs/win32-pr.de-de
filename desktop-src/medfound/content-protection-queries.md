---
description: Listet die Abfragen für die IDirect3DAuthenticatedChannel9::Query-Methode auf.
ms.assetid: 75e246c6-bf23-44d9-8fb3-46a6dc5324a5
title: Content Protection Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5aaa8c43cf722d13550ab4a1860e7a53780e7e82da7f374e28a7f599a22638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829090"
---
# <a name="content-protection-queries"></a>Content Protection Abfragen

Listet die Abfragen für die [**IDirect3DAuthenticatedChannel9::Query-Methode**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) auf.



| Statusanforderung                                                                                                                            | Beschreibung                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md)                                   | Gibt den Typ des E/A-Bus zurück, der zum Senden von Daten an die GPU verwendet wird.                                                                                                   |
| [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md)                                                           | Gibt den Typ des authentifizierten Kanals zurück.                                                                                                                  |
| [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md)                                                       | Gibt Handles an die kryptografische Sitzung und das Direct3D-Gerät zurück, die einem angegebenen DXVA-2-Decodergerät (DirectX Video Acceleration 2) zugeordnet sind. |
| [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)                   | Gibt den Verschlüsselungstyp zurück, der angewendet wird, bevor die CPU oder der Bus auf inhalte zugegriffen werden kann.                                                            |
| [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md)                                                         | Gibt ein Handle an das Gerät zurück, das diesem authentifizierten Kanal zugeordnet ist.                                                                          |
| [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)                         | Gibt einen der Verschlüsselungstypen zurück, mit denen Inhalt verschlüsselt werden kann, bevor er für die CPU oder den Bus zugänglich wird.                                     |
| [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)               | Gibt die Anzahl der Verschlüsselungstypen zurück, die zum Verschlüsseln von Inhalten verwendet werden können, bevor sie für die CPU oder den Bus zugänglich sind.                                  |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md)                                                                 | Gibt einen der Ausgabebezeichner zurück, der einer angegebenen kryptografischen Sitzung und einem Direct3D-Gerät zugeordnet ist.                                        |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md)                                                       | Gibt die Anzahl der Ausgabebezeichner zurück, die einer angegebenen kryptografischen Sitzung und einem Direct3D-Gerät zugeordnet sind.                                             |
| [**D3DAUTHENTICATEDQUERY-SCHUTZ \_**](d3dauthenticatedquery-protection.md)                                                             | Gibt die aktuelle Schutzebene für das Gerät zurück.                                                                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)                   | Gibt Informationen zu einem Prozess zurück, der freigegebene Ressourcen mit eingeschränktem Zugriff öffnen darf.                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)         | Gibt die Anzahl der Prozesse zurück, die freigegebene Ressourcen mit eingeschränktem Zugriff öffnen dürfen.                                                           |
| [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) | Gibt die Anzahl der geschützten freigegebenen Ressourcen zurück, die von jedem Prozess ohne Einschränkungen geöffnet werden können.                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Video-APIs](direct3d-video-apis.md)
</dt> <dt>

[GPU-basierte Content Protection](gpu-based-content-protection.md)
</dt> </dl>

 

 



