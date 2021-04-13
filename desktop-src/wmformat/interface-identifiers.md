---
title: Schnittstellen Bezeichner
description: Schnittstellen Bezeichner
ms.assetid: 009edcc0-34db-40a1-ae76-17492b11604a
keywords:
- Windows Media-Format-SDK, Schnittstellen Bezeichner (IID)
- Advanced Systems Format (ASF), Schnittstellen Bezeichner (IID)
- ASF (Advanced Systems-Format), Schnittstellen Bezeichner (IID)
- Schnittstellen Bezeichner (IID)
- IID (Schnittstellen Bezeichner)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253ca5b4110536c2207f7e18ab0f28067789df71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310840"
---
# <a name="interface-identifiers"></a>Schnittstellen Bezeichner

Beim Aufrufen der **QueryInterface** -Methode müssen Sie einen Schnittstellen Bezeichner (IID) verwenden. Eine IID ist ein Globally Unique Identifier (GUID)-Wert. Im Windows Media-Format-SDK ist die der IID zugewiesene Konstante für eine bestimmte Schnittstelle der Schnittstellen Name, dem ' IID ' vorangestellt ist \_ .

In der folgenden Tabelle sind die Schnittstellen Bezeichner und zugeordneten Konstanten für die Schnittstellen in diesem SDK aufgeführt.



| Schnittstelle                       | IID-Konstante                     | GUID                                 |
|---------------------------------|----------------------------------|--------------------------------------|
| **Inssbuffer**                  | IID \_ inssbuffer                  | E1CD3524-03D7-11d2-9EED-006097D2D7CF |
| **INSSBuffer2**                 | IID \_ INSSBuffer2                 | 4f 528693-1035-43fe-b428-757561ad3a68 |
| **INSSBuffer3**                 | IID \_ INSSBuffer3                 | c87ceaaf-75be-4bc4-84eb-ac2798507672 |
| **INSSBuffer4**                 | IID \_ INSSBuffer4                 | b6b8fd5a-32e2-49d4-a910-c26cc85465ed |
| **Iwmaddressaccess**            | IID \_ iwmaddressaccess            | BB3C6389-1633-4E92-AF14-9F3173BA39D0 |
| **IWMAddressAccess2**           | IID \_ IWMAddressAccess2           | 65a83fc2-3 e98-4D4D-81b5-2a742886b33d |
| **Iwmbackuprestore-Eigenschaften**       | IID \_ iwmbackuprestore-Eigenschaften       | 3c8e0da6-996f-4ff3-a1af-4838f9377e2e |
| **Iwmbandwidthsharing**         | IID \_ iwmbandwidthsharing         | ad694af1-f8d9-42f8-bc47-70311b0c4f9e |
| **Iwmclientconnections**        | IID \_ iwmclientconnections        | 73c66010-A299-41df-B1F 0-CCF 03b09c1c6 |
| **IWMClientConnections2**       | IID \_ IWMClientConnections2       | 4091571e-4701-4593-bb3d-d5f5f0c74246 |
| **Iwmcodecinfo**                | IID \_ iwmcodecinfo                | a970f41e-34de-4a98-b3ba-e4b3ca7528f0 |
| **IWMCodecInfo2**               | IID \_ IWMCodecInfo2               | aa65e273-b686-4056-91ec-dd768d4df710 |
| **IWMCodecInfo3**               | IID \_ IWMCodecInfo3               | 7e51f 487-4d93-4 AB4-27d0565adc51 |
| **Iwmkredentialcallback**       | IID \_ iwmkredentialcallback       | 342e0eb7-e651-450c-975b-2ace2c90c48e |
| **Iwmdeviceregistration**       | IID \_ iwmdeviceregistration       | f6211f03-8d21-4e94-93e6-8510805f2d99 |
| **Iwmdrmeditor**                | IID \_ iwmdrmeditor                | FF130EBC-A6C3-42A6-B401-C3382C3E08B3 |
| **Iwmdrmmessageparser**         | IID \_ iwmdrmmessageparser         | a73a0072-25a0-4c99-b4a5-ede8101a6c39 |
| **Iwmdrmreader**                | IID \_ iwmdrmreader                | d2827540-3ee7-432c-b14c-dc17f085d3b3 |
| **IWMDRMReader2**               | IID \_ IWMDRMReader2               | befe7a75-9F 1D-4075-b9d9-a3c37bda49a0 |
| **IWMDRMReader3**               | IID \_ IWMDRMReader3               | f28c0300-9baa-4477-a846-1744d9cbf 533 |
| **Iwmdrmtranszenryptor**          | IID \_ iwmdrmtranszenryptor          | 69059850-6e6f-4bb2-806f-71863ddfc471 |
| **Iwmdrmwriter**                | IID \_ iwmdrmwriter                | D6EA5DD0-12A0-43F4-90AB-A3FD451E6A07 |
| **IWMDRMWriter2**               | IID \_ IWMDRMWriter2               | 38ee7a94-40e2-4e10-aa3b-33sd3210ed5b |
| **IWMDRMWriter3**               | IID \_ IWMDRMWriter3               | a7184082-a4aa-4dde-ac9c-e75dbd1117ce |
| **Iwmheaderinfo**               | IID \_ iwmheaderinfo               | 96406bda-2b2b-11d3-b36b-00c04f 6108ff |
| **IWMHeaderInfo2**              | IID \_ IWMHeaderInfo2              | 15cf9781-454e-482e-b393-85fae487a810 |
| **IWMHeaderInfo3**              | IID \_ IWMHeaderInfo3              | 15cc68e3-27cc-4ecd-B222-3, g5d02d80bd5 |
| **Iwmimageingefo**                | IID \_ iwmimageingefo                | 9F 0aa3b6-7267-4d89-88f 2-ba915aa5c4c6 |
| **Iwmindexer**                  | IID \_ iwmindexer                  | 6d7cdc71-9888-11d3-8edc-00c04f 6109cf |
| **IWMIndexer2**                 | IID \_ IWMIndexer2                 | b70f1e42-6255-4df0-a6b9-02b212d9e2bb |
| **Iwminputmedia-Eigenschaften**          | IID \_ iwminputmedia-Eigenschaften          | 96406bd5-2b2b-11d3-b36b-00c04f 6108ff |
| **Iwmistream-Eigenschaften**             | IID \_ iwmistream-Eigenschaften             | 6816dad3-2b4b-4c8e-8149-874c3483a753 |
| **Iwmlanguagelist**             | IID \_ iwmlanguagelist             | DF683F00-2D49-4D8E-92B7-FB19F6A0DC57 |
| **Iwmlicenlbackup**            | IID \_ iwmlicenlbackup            | 05e5ac9f-3fb6-4508-BB43-a4067ba1ebe8 |
| **Iwmlicenserestore**           | IID \_ iwmlicenserestore           | C70B6334-a22e-4efb-A245-15E65A004A13 |
| **Iwmlicenserevocationagent**   | IID \_ iwmlicenserevocationagent   | 6967s2c9-4e26-4b57-8894-799880f-ac7b |
| **Iwmmedia-Eigenschaften**               | IID \_ iwmmedia-Eigenschaften               | 96406bce-2b2b-11d3-b36b-00c04f 6108ff |
| **IWMMetadataEditor**           | IID \_ IWMMetadataEditor           | 96406bd9-2b2b-11d3-b36b-00c04f 6108ff |
| **IWMMetadataEditor2**          | IID \_ IWMMetadataEditor2          | 203cffe3-2E18-4fdf-b59d-6e71530534cf |
| **Iwmmutualexclusion**          | IID \_ iwmmutualexclusion          | 96406bde-2b2b-11d3-b36b-00c04f 6108ff |
| **IWMMutualExclusion2**         | IID \_ IWMMutualExclusion2         | 302b57d?-89d1-4BA2-85c9-166b57c53eb91 |
| **Iwmoutputmedia-Eigenschaften**         | IID \_ iwmoutputmedia-Eigenschaften         | 96406bd7-2b2b-11d3-b36b-00c04f 6108ff |
| **Iwmpacketsize**               | IID \_ iwmpacketsize               | cdfb97ab-188f-40b3-b643-5b7903975c59 |
| **IWMPacketSize2**              | IID \_ IWMPacketSize2              | 8bfc2b9e-B646-4233-A877-1c6a7? 9669dc |
| **Iwmplayerhook**               | IID \_ iwmplayerhook               | e5b7ca9a-0f1c-4f66-9002-74ec50d8b304 |
| **Iwmprofile**                  | IID \_ iwmprofile                  | 96406bdb-2b2b-11d3-b36b-00c04f 6108ff |
| **IWMProfile2**                 | IID \_ IWMProfile2                 | 07e72d33-d94e-4be7-8843-60ae5ff7e5f5 |
| **IWMProfile3**                 | IID \_ IWMProfile3                 | 00ef96cc-a461-4546-8bcd-c9a28f 0e06f 5 |
| **Iwmprofilemanager**           | IID \_ iwmprofilemanager           | d16679f2-6ca0-472d-8d31-2f5d55aee155 |
| **IWMProfileManager2**          | IID \_ IWMProfileManager2          | 7a924e51-73c1-494d-8019-23d37ed9b89a |
| **Iwmprofilemanagerlanguage**   | IID \_ iwmprofilemanagerlanguage   | ba4dcc78-7ee0-4ab8-b27a-dbce8bc51454 |
| **Iwmpropertyvault**            | IID \_ iwmpropertyvault            | 72995a79-5090-42a4-9c8c-d9d0b6d34be5 |
| **Iwmproximityerkennung**       | IID \_ iwmproximityerkennung       | 6a9ld8ee-b651-4BF 0-B849-7d4ece79a2b1 |
| **Iwmreader**                   | IID \_ iwmreader                   | 96406bd6-2b2b-11d3-b36b-00c04f 6108ff |
| **Iwmreaderaccelerator**        | IID \_ iwmreaderaccelerator        | BDDC4D08-944D-4D52-A612-46C3FDA07DD4 |
| **Iwmreaderadvanced**           | IID \_ iwmreaderadvanced           | 96406bea-2b2b-11d3-b36b-00c04f 6108ff |
| **IWMReaderAdvanced2**          | IID \_ IWMReaderAdvanced2          | ae14a945-b90c-4d0d-9127-80d665f7d73e |
| **IWMReaderAdvanced3**          | IID \_ IWMReaderAdvanced3          | 5dc0674b-f 04b-4a4e-9F 2a-b1afde2c8100 |
| **IWMReaderAdvanced4**          | IID \_ IWMReaderAdvanced4          | 945a76a2-12ae-4d48-bd3c-cd1d90399b85 |
| **IWMReaderAdvanced5**          | IID \_ IWMReaderAdvanced5          | 24c44db0-55d1-49ae-a5cc-l13815e36363 |
| **IWMReaderAdvanced6**          | IID \_ IWMReaderAdvanced6          | 18a2e7f 8-428f -4acd-8a00-e64639bc93de |
| **Iwmreaderzuweisung**        | IID \_ iwmreaderzuweisung        | 9F 762fa7-A22e-428D-93c9-ac82f-afe5a |
| **Iwmreadercallback**           | IID \_ iwmreadercallback           | 96406bd8-2b2b-11d3-b36b-00c04f 6108ff |
| **Iwmreadercallbackadvanced**   | IID \_ iwmreadercallbackadvanced   | 96406beb-2b2b-11d3-b36b-00c04f 6108ff |
| **Iwmreadernetworkconfig**      | IID \_ iwmreadernetworkconfig      | 96406bec-2b2b-11d3-b36b-00c04f 6108ff |
| **IWMReaderNetworkConfig2**     | IID \_ IWMReaderNetworkConfig2     | d979a853-042b-4050-8387-c939db22013f |
| **Iwmreaderplaylistburn**       | IID \_ iwmreaderplaylistburn       | f28c0300-9baa-4477-a846-1744d9cbf 533 |
| **Iwmreaderstreamclock**        | IID \_ iwmreaderstreamclock        | 96406bed-2b2b-11d3-b36b-00c04f 6108ff |
| **Iwmreadertimecode**           | IID \_ iwmreadertimecode           | F369E2F0-E081-4FE6-8450-B810B2F410D1 |
| **Iwmreadertypenegotiziierung**    | IID \_ iwmreadertypenegotiation    | fdbe5592-81a1-41ea-93bd-735cad1adc5? |
| **Iwmregistercallback**         | IID \_ iwmregistercallback         | cf4b1f99-4de2-4e49-a363-252740d99bc1 |
| **Iwmregistereddevice**         | IID \_ iwmregistereddevice         | a4503bec-5508-4148-97ac-bfa75760a70d |
| **Iwmsbufferzucator**         | IID \_ iwmsbufferzuweisung         | 61103ca4-2033-11d2-9ef1-006097d2d7cf |
| **Iwmsinternaladminnetsource**  | IID \_ iwmsinternaladminnetsource  | 8bb23e5f-D127-4afb-8d02-ae5b05d54c78 |
| **IWMSInternalAdminNetSource2** | IID \_ IWMSInternalAdminNetSource2 | E74D58C3-CF77-4b51-AF17-744687C43EAE |
| **IWMSInternalAdminNetSource3** | IID \_ IWMSInternalAdminNetSource3 | 6b63d08e-4590-44af-9eb3-57ff1e73bf80 |
| **Iwmstatus Callback**           | IID \_ iwmstatus Callback           | 6d7cdc70-9888-11d3-8edc-00c04f 6109cf |
| **Iwmstreamconfig**             | IID \_ iwmstreamconfig             | 96406bdc-2b2b-11d3-b36b-00c04f 6108ff |
| **IWMStreamConfig2**            | IID \_ IWMStreamConfig2            | 7688d8cb-fc0d-43bd-9459-5a8dec200cfa |
| **IWMStreamConfig3**            | IID \_ IWMStreamConfig3            | cb164104-3aa9-45a7-9ac9-4daee131d6e1 |
| **Iwmstreamlist**               | IID \_ iwmstreamlist               | 96406bdd-2b2b-11d3-b36b-00c04f 6108ff |
| **Iwmstreampriorisierung**     | IID \_ iwmstreampriorisierung     | 8c1c6090-B8-4748-8ec3-dd1108ba1e77 |
| **Iwmsynkreader**               | IID \_ iwmsynkreader               | 9397f 121-7705-4dc9-b049-98b698188414 |
| **IWMSyncReader2**              | IID \_ IWMSyncReader2              | faed3d21-1b6b-4af7-8cb6-3e189bbc187b |
| **Iwmvideomedia-Eigenschaften**          | IID \_ iwmvideomedia-Eigenschaften          | 96406bcf-2b2b-11d3-b36b-00c04f6108ff |
| **Iwmwatermarkinfo**            | IID \_ iwmwatermarkinfo            | 6f 497062-f 2E2-4624-8ea7-9dd40d81fc8d |
| **Iwmwriter**                   | IID \_ iwmwriter                   | 96406bd4-2b2b-11d3-b36b-00c04f 6108ff |
| **Iwmschreibadvanced**           | IID \_ iwmbeschreiteradvanced           | 96406be3-2b2b-11d3-b36b-00c04f 6108ff |
| **IWMWriterAdvanced2**          | IID \_ IWMWriterAdvanced2          | 962dc1ec-C046-4db8-9cc7-26ceae500817 |
| **IWMWriterAdvanced3**          | IID \_ IWMWriterAdvanced3          | 2cd6492d-7c37-4e76-9d3b-59261183a22e |
| **Iwmschreibfilesink**           | IID \_ iwmschreiterfilesink           | 96406be5-2b2b-11d3-b36b-00c04f 6108ff |
| **IWMWriterFileSink2**          | IID \_ IWMWriterFileSink2          | 14282ba7-4aef-4205-8ce5-c229035a05bc |
| **IWMWriterFileSink3**          | IID \_ IWMWriterFileSink3          | 3fea4feb-2945-47a7-a1dd-c53a8fc4c45c |
| **Iwmschreibfilesinkdataunit**   | IID \_ iwmbeschreiterfilesinkdataunit   | 633392f 0-be5c-486b-a09c-10669c7a6c27 |
| **Iwmschreiternetworksink**        | IID \_ iwmbeschreiternetworksink        | 96406be7-2b2b-11d3-b36b-00c04f 6108ff |
| **Iwmbeschreiterpostview**           | IID \_ iwmbeschreiterpostview           | 81e20ce4-75ef-491a-8004-fc53c45bdc3e |
| **Iwmschreiterpostviewcallback**   | IID \_ iwmschreiterpostviewcallback   | d9d6549d-a193-4f24-b308-03123d9b7f8d |
| **IWMWriterPreprocess**         | IID \_ IWMWriterPreprocess         | fc54a285-38c4-45b5-aa23-85b9f7cb424b |
| **Iwmschreibpushsink**           | IID \_ iwmschreibpushsink           | DC10E6A5-072C-467D-BF57-6330A9DDE12A |
| **Iwmschreibsink**               | IID \_ iwmschreitersink               | 96406be4-2b2b-11d3-b36b-00c04f 6108ff |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**GUID-Werte**](guid-values.md)
</dt> </dl>

 

 




